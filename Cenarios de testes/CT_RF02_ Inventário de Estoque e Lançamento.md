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
## video:

------------------------------------------------------------------------

## Caso de Teste 02: Lançamento de inventário com ajuste de estoque.
ID	Descrição
C01-CT02	O sistema deve ajustar o saldo físico e contábil após contagem.
**Pré-condições**
Produtos importados previamente no sistema.
**Passos**
DADO que estamos na tela de Contagem Física
E informamos as quantidades reais contadas
QUANDO clicarmos em “Validar Inventário”
ENTÃO o sistema deve recalcular e ajustar o saldo contábil no banco de dados.
Critérios de aceitação
A diferença entre saldo físico e contábil deve ser atualizada na tabela produto.
## video:



## Caso de Teste: Tentativa de importar XML inválido
ID: C01-CT03
Descrição: O sistema deve rejeitar um arquivo XML com estrutura incorreta.
**Pré-condições**:
 O usuário deve estar logado e com acesso à tela de importação.
**Passos**: DADO que estamos na tela de Inventário
E selecionamos um arquivo XML com estrutura incorreta
QUANDO clicarmos em 'Importar'
ENTÃO o sistema deve exibir uma mensagem de erro 'Arquivo inválido'.
Critérios de Aceitação: Nenhum produto deve ser cadastrado e a mensagem deve ser clara.
## video:



## Caso de Teste: Validação de reconciliação de estoque
ID: C01-CT04
Descrição: Após o lançamento, o sistema deve refletir corretamente a diferença entre estoque
físico e contábil.
**Pré-condições**: Inventário lançado e validado.
**Passos**: DADO que um inventário foi finalizado
QUANDO consultamos o relatório de ajustes
ENTÃO a diferença entre o saldo físico e contábil deve estar refletida no BD (produto.estoq_pro).
Critérios de Aceitação: O saldo ajustado deve corresponder à contagem física.
## video: