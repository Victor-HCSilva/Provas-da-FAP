# Provas-da-FAP
provas da fap 2024 Aluno Victor Hugo C. da silva
o código consiste nq base normal padrão do python não exige muitas especificações
relevantes por tanto que haja a versão mais atual do python o código vai funcionar.

***Sistema simples de gerenciamento de dados (VERSÃO 1, prova_v1)***
Sobre as funções:
movimentações grava em um arquivo texto as operações do usuário como cadastro de novas contas (NC),
deleção (D), extrato(E). O restante é apenas manipulação de lista de dicionários. Em breve mais.(2024-08-28)


***Sistema simples de gerenciamento de dados (VERSÃO 2, prova_v2)***


----SOBRE  O QUE É O CÓDIGO:-----
linguagem python

O código prova_V2.py é um sistema bancário simples com dados
salvos no Mysql (usando a biblioteca mysql.connector). 

TABELAS MySQL:
existem duas tabelas que previamente são necessárias a tabela "banco"
e "movimentacoes", onde a tabela banco guarda:  nome, saldo,
data, id, e numero da  conta. A tabela "movimentacoes" salva apenas
id, data, saldo e transações: (saldo, depósito), respectivamente "S" para
saldo e "D" para depósito. o id da tabela "movimentacoes" é o mesmo 
da tabela "banco". As tabelas usadas estão no começo do código.

------FUNÇÕES:------

 - FUNÇÕES AUXILIARES( "conexao_ao_banco" e "mostrar_id"):

retorna uma conexão ao banco para facilitar a consulta em todas 
as outras funções, é uma função auxiliar. Juntamente a função "mostra_id"
retorna o id (id_cliente) do cliente/usuário, que é muito usado no código
para gerar uma segurança em relação às consultas no banco de dados.

 - ALTERAÇÕES( "mudanca"):

serve para mudar mudar o nome ou número da conta, não
é possível mudar o id pois ele é unico para cada pessoa cadastrada.

- EXIBIR EXTRATO  ( "extrato"):

Serve para exibir o extrato, ao chamar a função ela mostrar tudo sobre
a conta desde a data  deciação até as transações feitas.

- CRIAR UMA CONTA ("criar_conta"):

Cria uma conta nova, ou seja faz uma consulta e insere uma nova
pessoa de id auto-incrementado  de saldo zero, a data é colocada
automaticamente usando a biblioteca datetime (from datetime import 
datetime, data=str(datetime.now())), e po fim o número correspondente
a conta tem que ser digitado.

- DEPOSITAR DINHEIRO ( "depositar"):

Apenas faz uma consulta para somar o saldo existente nas tabelas.

- SACAR DINHEIRO ("sacar"):

Apenas consulta a tabela e retira o valor digitado/exigido.

 - APAGAR CONTA ("deletar"):

Deleta uma conta, dá o seguinte comando no banco de dados:
DELETE FROM banco WHERE numero conta = ? and nome = ?
esses parâmetros são para que exista uma consistência e segurança 
maior dos dados já que é necessário oferecer corretamente o nome
do titular da conta junto do número da conta (função 
"criar_conta").

 - REGISTRO ("salvar_movimentacoes"):

Registra as operações de Saque e Depósito respectivamente com
as siglas "S" e "D".


----------EXTRA:-------

Em resumo para todas as operações existe uma função. 
Existe um certo tratamento de possíveis erros, há trechos 
específicos que podem não responder muito bem se houver 
esforço para encontrar erros. Todo o código é simples de entender,
porém um pouco denso o que torna fácil errar em um ponto ou outro.
Melhorarei! Obrigado!





