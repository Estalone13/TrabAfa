## Cenário 03: Processamento de Venda (PDV)

## Caso de Teste: Venda com desconto e pagamento misto
ID: C02-CT01
**Descrição**: O sistema deve registrar venda com desconto e pagamento misto.
**Pré-condições**: Caixa deve estar aberto e produtos cadastrados.
**Passos**: DADO que iniciamos uma nova venda
E adicionamos 5 itens ao carrinho
E aplicamos um desconto em 1 item
E selecionamos forma de pagamento 'cartão 70%' e 'dinheiro 30%'
QUANDO clicarmos em 'Finalizar Venda'
ENTÃO a venda deve ser gravada e o caixa atualizado corretamente.
Critérios de Aceitação: Os valores totais e tipos de pagamento devem ser refletidos na tabela
caixa e itcaixa.
## video:



## Caso de Teste: Venda sem produtos
ID: C02-CT02
**Descrição**: O sistema deve impedir finalizar venda sem itens.
**Pré-condições**: Caixa aberto.
Passos: DADO que iniciamos uma nova venda
E não adicionamos nenhum produto
QUANDO clicarmos em 'Finalizar Venda'
ENTÃO deve ser exibida mensagem de erro 'Nenhum item adicionado'.
Critérios de Aceitação: A venda não deve ser registrada no banco.
## video:




## Caso de Teste: Desconto acima do permitido
ID: C02-CT03
**Descrição**: O sistema deve impedir aplicar desconto maior que o limite permitido (ex: 20%).
**Pré-condições**: Produto cadastrado e limite configurado.
**Passos**: DADO que iniciamos uma venda
E aplicamos 50% de desconto em um item
QUANDO clicarmos em 'Confirmar'
ENTÃO o sistema deve recusar e exibir 'Desconto inválido'.
Critérios de Aceitação: Nenhum desconto fora do limite deve ser aceito.
## video: