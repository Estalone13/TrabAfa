✅ Relatório Final de Execução de Testes - Sistema AFA

Sistema testado: AFA Sistemas
Responsável: Pablo Felipe de Almeida Ferreira
Data de execução: 20/11/2025
Ambiente: Servidor Interno / Firebird
Ferramentas: AFA PDV, IBExpert, Jam.dev

📊 Resumo da Execução
Total de Casos	Passaram	Falharam	Bugs Encontrados
16	                11	        5	     5

🔍 Cobertura por Módulo
Código RF	Módulo	Casos	Passaram	Bugs	ID(s)
RF01	Inventário de Estoque	4	3	1	BUG-001
RF02	PDV - Vendas	3	2	1	BUG-002
RF03	Compras	3	3	0	-
RF04	Clientes	3	2	2	BUG-004, BUG-005
RF06	Fechamento de Caixa	3	2	1	BUG-003

🧮 Resumo dos Bugs
ID	Título	Severidade	Status
BUG-001	XML inválido não tratado	Alta	Aberto
BUG-002	Duplicidade em pagamento misto	Alta	Aberto
BUG-003	Fechamento bloqueado com saldo zero	Média	Aberto
BUG-004	Cadastro duplicado de CPF	Alta	Aberto
BUG-005	Limite de crédito não atualizado	Média	Aberto
📈 Indicadores

Casos de Sucesso: 68%
Falhas Identificadas: 32%
Severidade Alta: 3 bugs
Severidade Média: 2 bugs

📁 Evidências

Vídeos e prints hospedados no Jam.dev

Consultas SQL e logs de BD armazenados em IBExpert

Planilha “Execução de Testes - AFA.xlsx” anexada

✅ Conclusão

A execução dos testes do Sistema AFA apresentou boa estabilidade geral, com destaque positivo para os módulos Compras e Relatórios.
Entretanto, foram identificadas falhas críticas nos módulos PDV, Inventário e Gestão de Clientes, que impactam diretamente o controle financeiro e integridade de dados.

🔍 Causa raiz provável:

Falhas de validação de entrada (XML e CPF duplicado)

Sincronização incorreta entre interface e banco (limite de crédito e fechamento de caixa)

📘 Recomendações:

Implementar validação de estrutura XML antes do import.

Corrigir trigger de atualização de crédito no banco.

Reforçar validações no fechamento de caixa.