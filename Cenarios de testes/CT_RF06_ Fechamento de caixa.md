## Cenário 06: Fechamento de Caixa

## Caso de Teste: Fechamento de múltiplos caixas simultâneos
ID: C06-CT01
**Descrição**: O sistema deve permitir fechar 1 caixa e validar totais.
**Pré-condições**: Deve haver 1 caixa aberto com movimentações registradas.
**Passos**: DADO que 1 caixas está aberto
E que o caixa possui venda com diferentes formas de pagamento
QUANDO clicarmos em 'Fechar Caixa'
ENTÃO o sistema deve conciliar os total no caixa e gerar relatório final.
Critérios de Aceitação: Os totais dos relatórios devem coincidir com os registros da tabela caixa e
itcaixa.
## video:https://jam.dev/c/085691f2-6286-4298-ba7a-9b0c830dd098


## Caso de Teste: Tentativa de fechar caixa com saldo pendente
ID: C06-CT02
**Descrição**: O sistema deve impedir o fechamento se houver lançamentos não finalizados.
**Pré-condições**: Caixa aberto e venda não concluída.
Passos: DADO que o caixa contém lançamentos pendentes
QUANDO clicarmos em 'Fechar Caixa'
ENTÃO o sistema deve exibir 'Existem lançamentos pendentes'.
Critérios de Aceitação: O caixa deve permanecer aberto até que tudo esteja conciliado.
## video:https://jam.dev/c/085691f2-6286-4298-ba7a-9b0c830dd098 
ele aparece a mensagem porem deixa eu fechar mesmo assim.


## Caso de Teste: Reabertura de caixa fechado
ID: C06-CT03
**Descrição**: O sistema deve permitir reabrir um caixa fechado para conferência.
**Pré-condições**: Caixa encerrado com data anterior.
**Passos**: DADO que um caixa foi fechado
QUANDO clicarmos em 'Reabrir Caixa'
ENTÃO o sistema deve permitir a edição somente para conferência, sem alterar os lançamentos.
Critérios de Aceitação: A reabertura deve ser registrada em log e não alterar saldos
## video:https://jam.dev/c/c4d1d87b-02fd-4ccc-8eac-275f2fcc3225
ele reabre porem sumiu os dados
