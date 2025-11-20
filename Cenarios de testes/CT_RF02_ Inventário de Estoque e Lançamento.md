## Cenário 01: Inventário de Estoque

## Caso de Teste 01: Importação de produtos via XML.

ID	Descrição
C01-CT01	O sistema deve permitir importar produtos fictícios via arquivo XML.
**Pré-condições**
O usuário deve ter acesso ao (módulo de Inventário de Estoque).
**Passos**
DADO que estamos na tela de Inventário de Estoque
E selecionamos a opção “Importar XML”
E escolhemos um arquivo XML válido com produtos fictícios
QUANDO clicarmos em “Importar”
ENTÃO os produtos devem ser cadastrados na base de dados.
Critérios de aceitação
Todos os produtos do XML devem aparecer na listagem de produtos.

## video:https://jam.dev/c/f96959bd-09c3-41a4-a283-bd77c9c008f4



## Caso de Teste 02: Tentativa de importar XML inválido
ID: C01-CT02
Descrição: O sistema deve rejeitar um arquivo XML com estrutura incorreta.
**Pré-condições**:
 O usuário deve estar logado e com acesso à tela de importação.
**Passos**: DADO que estamos na tela de Inventário
E selecionamos um arquivo XML com estrutura incorreta
QUANDO clicarmos em 'Importar'
ENTÃO o sistema deve exibir uma mensagem de erro 'Arquivo inválido'.
Critérios de Aceitação: Nenhum produto deve ser cadastrado e a mensagem deve ser clara.

## video:https://jam.dev/c/f5c7b1da-5ae6-4605-a665-590262febc64



