🐞 Relatório de Bugs - Sistema AFA

Software: AFA Sistemas
Responsável QA: Pablo Felipe de Almeida Ferreira,Marlon Nunes Apolonio
Data: 20/11/2025

🐞 Bug 01: XML de importação não reconhecido
ID	Descrição
BUG-001	O sistema não reconhece XMLs com campos adicionais e exibe erro genérico “Arquivo inválido”.

Severidade: Alta
Prioridade: Alta
Status: Aberto

Passos:

Acessar módulo de Inventário

Selecionar “Importar XML”

Escolher arquivo com campos não mapeados

Comportamento Esperado: Mensagem clara indicando erro de estrutura.
Comportamento Obtido: Erro genérico sem detalhe.

Evidência: Vídeo Jam.dev

🐞 Bug 02: Venda com pagamento misto não salva corretamente
ID	Descrição
BUG-002	Venda com 70% cartão e 30% dinheiro gera duplicidade no fechamento de caixa.

Severidade: Alta
Prioridade: Alta
Status: Aberto

Passos:

Criar venda no PDV

Escolher “Pagamento Misto”

Fechar venda

Comportamento Esperado: Total correto e único registro em caixa.
Comportamento Obtido: Duas entradas duplicadas no BD (itcaixa).

Evidência: Vídeo Jam.dev

🐞 Bug 03: Fechamento de caixa bloqueado com saldo zero
ID	Descrição
BUG-003	Mesmo sem pendências, o sistema exibe “Existem lançamentos pendentes” ao tentar fechar caixa.

Severidade: Média
Prioridade: Média
Status: Aberto

Evidência: Vídeo Jam.dev

🐞 Bug 04: Cadastro duplicado de clientes com mesmo CPF
ID	Descrição
BUG-004	O sistema permite cadastrar dois clientes com o mesmo CPF sem validação.

Severidade: Alta
Prioridade: Alta
Status: Aberto

Evidência: Vídeo Jam.dev

🐞 Bug 05: Atualização de limite de crédito não refletida no BD
ID	Descrição
BUG-005	Alterações de limite de crédito não são gravadas na tabela cliente.

Severidade: Média
Prioridade: Alta
Status: Aberto

Evidência: Vídeo Jam.dev