## Cenário 04: Gestão de Clientes

## Caso de Teste: Cadastro e controle de crédito
ID: C04-CT01
**Descrição**: O sistema deve registrar clientes, dependentes e aplicar regras de crédito.
**Pré-condições**: O módulo de Clientes deve estar disponível.
**Passos**: DADO que cadastramos 6 clientes (PJ e PF)
E adicionamos dependentes para 2 deles
E habilitamos limite de crédito para 2 clientes
QUANDO realizarmos compras acima do limite
ENTÃO o sistema deve bloquear a compra automaticamente.
Critérios de Aceitação: O cliente deve ser impedido de realizar compras acima do limite definido.
## video:


## Caso de Teste: Atualização de limite de crédito
ID: C04-CT02
**Descrição**: O sistema deve permitir ajustar o limite de crédito de um cliente ativo.
**Pré-condições**: Cliente cadastrado e com limite ativo.
**Passos**: DADO que acessamos o cadastro do cliente
E alteramos o valor do limite de crédito
QUANDO clicarmos em 'Salvar'
ENTÃO o novo limite deve ser gravado e refletido nas próximas compras.
Critérios de Aceitação: O valor alterado deve ser exibido corretamente no BD e nas telas de
venda.
## video:

## Caso de Teste: Cadastro duplicado de CPF/CNPJ
ID: C04-CT03
**Descrição**: O sistema deve impedir cadastrar cliente com CPF ou CNPJ já existente.
**Pré-condições**: Cliente existente com CPF/CNPJ cadastrado.
**Passos**: DADO que tentamos cadastrar novo cliente
E informamos CPF já existente
QUANDO clicarmos em 'Salvar'
ENTÃO o sistema deve exibir a mensagem 'CPF já cadastrado'.
Critérios de Aceitação: Nenhum novo registro deve ser criado com dados duplicados.
## video: