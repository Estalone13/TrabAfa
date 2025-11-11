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
## video:

## Caso de Teste: Pagamento parcial de parcelas
ID: C05-CT02
**Descrição**: O sistema deve aceitar pagamento parcial da segunda parcela de uma compra.
**Pré-condições**: Compra gerada com 5 parcelas.
**Passos**: DADO que acessamos o módulo de Contas a Pagar
E localizamos a segunda parcela
QUANDO efetuamos pagamento parcial
ENTÃO o sistema deve atualizar o saldo pendente corretamente.
Critérios de Aceitação: A coluna de saldo da parcela deve refletir o valor restante.
## video:


## Caso de Teste: Tentativa de recebimento sem nota fiscal
ID: C05-CT03
**Descrição**: O sistema deve impedir o recebimento de produtos sem nota fiscal associada.
**Pré-condições**: Pedido de compra criado sem documento fiscal.
**Passos**: DADO que acessamos o módulo de Recebimento
E tentamos dar entrada em produtos sem nota
QUANDO clicarmos em 'Confirmar'
ENTÃO o sistema deve exibir 'Nota fiscal obrigatória'.
Critérios de Aceitação: O estoque não deve ser atualizado.
## video: