## Cenário 06: Fechamento de Caixa

## Caso de Teste: Fechamento de múltiplos caixas simultâneos
ID: C06-CT01
**Descrição**: O sistema deve permitir fechar 3 caixas simultaneamente e validar totais.
**Pré-condições**: Deve haver 3 caixas abertos com movimentações registradas.
**Passos**: DADO que 3 caixas estão abertos
E cada caixa possui vendas com diferentes formas de pagamento
QUANDO clicarmos em 'Fechar Caixa'
ENTÃO o sistema deve conciliar os totais de cada caixa e gerar relatório final.
Critérios de Aceitação: Os totais dos relatórios devem coincidir com os registros da tabela caixa e
itcaixa.
## video:


## Caso de Teste: Tentativa de fechar caixa com saldo pendente
ID: C06-CT02
**Descrição**: O sistema deve impedir o fechamento se houver lançamentos não finalizados.
**Pré-condições**: Caixa aberto e venda não concluída.
Passos: DADO que o caixa contém lançamentos pendentes
QUANDO clicarmos em 'Fechar Caixa'
ENTÃO o sistema deve exibir 'Existem lançamentos pendentes'.
Critérios de Aceitação: O caixa deve permanecer aberto até que tudo esteja conciliado.
## video:


## Caso de Teste: Reabertura de caixa fechado
ID: C06-CT03
**Descrição**: O sistema deve permitir reabrir um caixa fechado para conferência.
**Pré-condições**: Caixa encerrado com data anterior.
**Passos**: DADO que um caixa foi fechado
QUANDO clicarmos em 'Reabrir Caixa'
ENTÃO o sistema deve permitir a edição somente para conferência, sem alterar os lançamentos.
Critérios de Aceitação: A reabertura deve ser registrada em log e não alterar saldos
## video: