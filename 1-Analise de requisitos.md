## Requisitos Funcionais Detalhados para Testes Manuais - Sistema AFA


📦 RF01 - Inventário de Estoque

Descrição: Permitir o controle e reconciliação do estoque físico com o sistema.

Funcionalidades esperadas:

Importação de produtos fictícios via arquivo XML.

Realização da contagem física simulada.

Lançamento do inventário com ajustes automáticos no saldo.

Geração de relatório de ajustes e reconciliação entre saldo contábil e físico.

Validação em banco de dados da consistência entre os valores ajustados.



💰 RF02 - Processamento de Venda (PDV)

Descrição: Controlar o processo completo de venda, desde a abertura até o fechamento de caixa.

Funcionalidades esperadas:

Iniciar nova venda com múltiplos itens.

Aplicar desconto promocional em item selecionado.

Realizar pagamento misto (ex: 70% cartão, 30% dinheiro).

Emitir comprovante e registrar operação no caixa.

Validar integridade dos cálculos e lançamentos financeiros no banco.



🏦 RF03 - Compra com Fornecedores

Descrição: Gerenciar o fluxo de aquisição de produtos junto aos fornecedores.

Funcionalidades esperadas:

Cadastrar novos fornecedores no sistema.

Gerar pedido de compra com até 10 itens.

Registrar contas a pagar parceladas (ex: 5 parcelas).

Permitir pagamento total e parcial das parcelas.

Atualizar o estoque somente após confirmação de recebimento.

Validar movimentação de estoque e caixa no banco de dados.



👥 RF04 - Gestão de Clientes

Descrição: Gerenciar informações de clientes (PF e PJ), dependentes e limites de crédito.

Funcionalidades esperadas:

Cadastrar novos clientes e dependentes.

Habilitar e editar limite de crédito individual.

Registrar compras para clientes e dependentes.

Bloquear compras acima do limite permitido.

Gerar relatório de contas a receber e histórico de compras.

Validar bloqueios e registros na base de dados (cliente e cont_rec).



💼 RF05 - Fechamento de Caixa

Descrição: Controlar a finalização e conferência dos caixas diários da empresa.

Funcionalidades esperadas:

Simular operações de 3 caixas simultâneos.

Realizar vendas com tipos de documentos variados (cartão, dinheiro, PIX).

Registrar retiradas e sangrias de caixa.

Fechar o caixa e conciliar os tipos de documentos.

Gerar relatório final de conferência e validação no banco (caixa, itcaixa).

Garantir integridade do saldo contábil ao encerrar o dia.



⚙️ RF06 - Validações de Banco de Dados

Descrição: Garantir que todas as operações do sistema estejam refletidas corretamente nas tabelas do banco de dados Firebird.

Funcionalidades esperadas:

C1: Verificar atualização correta da tabela produto.

C2: Confirmar integridade da tabela caixa após vendas e fechamentos.

C3: Validar campo estoq_pro em produto após inventário e compras.

C4: Conferir dados de cont_rec e cliente para histórico e crédito.

C5: Validar status (aberto/fechado) e saldo de caixa e itcaixa.



🧮 RF07 - Controle Financeiro

Descrição: Gerenciar recebimentos, pagamentos e conciliação financeira da empresa.

Funcionalidades esperadas:

Registro de entradas e saídas financeiras.

Geração de relatórios de movimentações diárias.

Controle de contas a pagar e receber vinculadas a compras e vendas.

Atualização automática do saldo de caixa após transações.



🧾 RF08 - Relatórios Gerenciais

Descrição: Disponibilizar relatórios detalhados sobre movimentações de estoque, clientes, fornecedores e caixa.

Funcionalidades esperadas:

Relatório de ajustes de inventário.

Relatório de vendas diárias por tipo de pagamento.

Relatório de contas a receber e pagar.

Relatório consolidado de fechamento de caixa.

Exportação em formatos CSV ou PDF.



🔐 RF09 - Controle de Acesso (Login AFA)

Descrição: Permitir que usuários autorizados acessem o sistema AFA com suas credenciais.

Funcionalidades esperadas:

Login com usuário e senha (ex: alfasi\usuario).

Validação de autenticação interna ou via RDP.

Exibição de mensagem de erro em caso de credenciais inválidas.

Acesso diferenciado conforme perfil (Gerente, Caixa, Administrador).



🧱 RF10 - Registro de Erros (BUG Tracking)

Descrição: Controlar e documentar falhas encontradas durante o uso do sistema.

Funcionalidades esperadas:

Permitir cadastro de bug contendo título, descrição, resultado esperado e evidência.

Associar bug a ambiente de execução (IBExpert, Firebird, PDV).

Anexar vídeo ou imagem da falha.

Consultar histórico de bugs registrados.