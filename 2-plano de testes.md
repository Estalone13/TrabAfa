🧪 Plano de Testes - Sistema AFA

📌 1. Identificação

Nome do Projeto: Sistema AFA - Automação de Fluxos Administrativos

Versão Avaliada: 1.0 (Ambiente Local / IBExpert)

Ambiente de Testes: Servidor interno 172.16.11.230 e 186.236.35.2:33899

Banco de Dados: Firebird (C:\AFA Sistemas\Assistentes\IBExpert)

Tipo de Teste: Teste Funcional Manual

Data do Documento: 20/11/2025

Responsável: Pablo Felipe de Almeida Ferreira,MArlon Nunes Apolonio


🎯 2. Objetivo

Validar o comportamento funcional do sistema AFA, assegurando que todos os módulos críticos (Inventário, Vendas, Compras, Clientes e Caixa) funcionem conforme os requisitos estabelecidos, mantendo integridade de dados e consistência entre sistema e banco de dados.


🧩 3. Escopo

Incluído:

Login Afa

Inventário de Estoque

Processamento de Venda (PDV)

Compra com Fornecedores

Gestão de Clientes

Fechamento de Caixa

Relatórios e Validações BD

Excluído:

Integrações externas (sistemas de terceiros)

Testes de carga e performance

Testes mobile e responsividade



🔧 4. Ferramentas Utilizadas

IBExpert (para consultas SQL e validações BD)

AFA Sistemas (versão local e PDV)

Planilha Excel / Google Sheets (controle de testes e bugs)

Jam.dev (gravação de vídeos de evidência)

Snipping Tool / Lightshot (capturas de tela)


🧪 5. Técnicas de Teste

Particionamento de equivalência

Análise de valor limite

Caminho feliz (Happy Path)

Testes negativos (inputs inválidos)

Testes exploratórios


📄 6. Critérios de Aceitação

Todas as funções devem executar conforme o comportamento esperado.

Nenhum bug crítico deve permanecer sem correção.

Dados no banco devem refletir exatamente as ações realizadas no sistema.

Mensagens de erro e sucesso devem ser claras e consistentes.


🚦 7. Critérios de Saída (Exit Criteria)

Todos os casos de teste executados e documentados.

Evidências (prints e vídeos) anexadas no repositório.

Falhas registradas e reavaliadas após correção.

Documentação final entregue dentro do prazo.

⏱️ 8. Cronograma Estimado
Atividade	Data Início	Data Fim
Planejamento de Testes	10/11/2025	10/11/2025
Criação de Casos de Teste	11/11/2025	13/11/2025
Execução dos Testes Manuais	14/11/2025	19/11/2025
Registro e Report de Bugs	19/11/2025	20/11/2025
Entrega Final	20/11/2025	20/11/2025


📋 9. Módulos a Serem Testados
Código RF	Módulo	Prioridade
RF01	Inventário de Estoque	Alta
RF02	PDV - Vendas	Alta
RF03	Compras com Fornecedores	Alta
RF04	Gestão de Clientes	Média
RF05	Fechamento de Caixa	Alta
RF06	Validações BD	Alta
RF07	Controle Financeiro	Média
RF08	Relatórios Gerenciais	Média
RF09	Login / Acesso	Alta
RF10	Registro de Bugs	Média


🐞 10. Gestão de Defeitos

Cada bug deve conter:

ID, Título e Descrição

Passos para reprodução

Resultado esperado x obtido

Evidência (imagem/vídeo)

Severidade e Status

Ferramenta de controle: Planilha de Bugs + Jam.dev

📌 11. Riscos Identificados
Risco	Impacto	Mitigação
Falha de comunicação com banco Firebird	Alto	Reconfigurar caminho do BD
XML inválido durante importação	Médio	Implementar validação prévia
Fechamento de caixa com saldo incorreto	Alto	Testar conciliação detalhada


📁 12. Entregáveis

Plano de Testes (PDF ou Markdown)

Casos de Teste (planilha e documento)

Evidências (prints e vídeos)

Relatório de Bugs

Relatório Final de Execução