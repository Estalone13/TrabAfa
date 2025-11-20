## Cenário 05: Compra com Fornecedores

## Caso de Teste: Cadastro de fornecedor e pedido de compra
ID: C05-CT01
**Descrição**: O sistema deve permitir cadastrar novo fornecedor e gerar pedido de compra.
**Pré-condições**: Usuário deve ter acesso ao módulo de Compras.
**Passos**: DADO que acessamos o módulo de Compras
E cadastramos um novo fornecedor
E geramos um pedido com 10 itens
QUANDO clicarmos em 'Salvar Pedido'
ENTÃO o pedido deve ser gravado e o estoque atualizado apenas após recebimento.
Critérios de Aceitação: O estoque só deve aumentar após o status do pedido mudar para
'Recebido'.
## video:https://jam.dev/c/c4d1d87b-02fd-4ccc-8eac-275f2fcc3225

## Caso de Teste: Tipo de documento sem preencher
 ID:C03-CT03                                                              
**Descrição**: O Sistema deve recusar finalização de compra sem um tipo de documento.
 **Pré-condições**:Estar finalizando uma compra.                                            
 **Passos**:DADO que o usuário cria uma nova compra           
E chega para finalizar uma compra
E deixa sem um tipo de documento ao finalizar
QUANDO selecionar a clicar em salvar
ENTÃO deve exibir uma mensagem de erro.
Critérios de Aceitação                                           
Mensagem de alerta: É necessário informar o tipo de documento.

## video:https://jam.dev/c/6ef1e8b8-ee07-4e11-904c-2075660adad5


## Caso de Teste: Tentativa de recebimento sem nota fiscal
ID: C05-CT03
**Descrição**: O sistema deve impedir o recebimento de produtos sem nota fiscal associada.
**Pré-condições**: Pedido de compra criado sem documento fiscal.
**Passos**: DADO que acessamos o módulo de Recebimento
E tentamos dar entrada em produtos sem nota
QUANDO clicarmos em 'Confirmar'
ENTÃO o sistema deve exibir 'Nota fiscal obrigatória'.
Critérios de Aceitação: O estoque não deve ser atualizado.
## video:https://jam.dev/c/17927a84-a0be-4fa4-8148-6ad5c434cce7
Não permitiu por conta de não ter documento preenchido na compra