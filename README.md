📦 Projeto de Banco de Dados para Sistema de E-commerce
Este repositório contém o esquema de banco de dados para um sistema de e-commerce completo, projetado para gerenciar clientes, produtos, pedidos, entregas e fornecedores de forma eficiente e escalável. Este projeto foi desenvolvido para fornecer uma base sólida para operações de comércio eletrônico, desde o processamento de pedidos até a rastreabilidade de entregas.

🗂️ Estrutura do Banco de Dados
A modelagem do banco de dados inclui as seguintes principais entidades:

🧑‍💼 Cliente
A entidade Cliente armazena informações essenciais de usuários do sistema, podendo ser tanto pessoas físicas quanto jurídicas.

idCliente: Identificador único do cliente.
Nome: Nome completo do cliente.
Endereço: Endereço de entrega.
Pagamento: Tipo de pagamento preferido.
👥 Pessoa Física & Pessoa Jurídica
Informações específicas sobre os tipos de clientes:

Pessoa Física: Inclui atributos como CPF.
Pessoa Jurídica: Inclui atributos como CNPJ e nome empresarial.
🛒 Pedido
A entidade Pedido representa as compras realizadas pelos clientes, armazenando detalhes fundamentais para a gestão de pedidos.

idPedido: Identificador único do pedido.
Compra: Detalhes dos itens comprados.
Endereço: Endereço de entrega do pedido.
Status da Entrega: Indica o status da entrega (ex.: "Pendente", "Em transporte", "Entregue").
Frete: Valor do frete associado ao pedido.
🚚 Entrega
A entidade Entrega gerencia o processo de entrega de pedidos e seu rastreamento.

Entregador_idEntregador: Referência ao entregador responsável.
Pedido_idPedido: Chave estrangeira para o pedido correspondente.
Status de Entrega: Estado atual da entrega.
Código de Rastreamento: Código de rastreamento para acompanhamento.
🏷️ Produtos & Estoque
Entidades que armazenam informações sobre os produtos disponíveis e seu estoque.

Produtos: Inclui detalhes como categoria, descrição e preço.
Produtos_has_Estoque: Relação que liga os produtos ao estoque disponível e sua quantidade.
🤝 Fornecimento
A entidade Fornecimento mapeia a relação entre fornecedores e os produtos que oferecem.

Fornecedor_idFornecedor: Identificador do fornecedor.
Produtos_idProdutos: Referência aos produtos fornecidos.
📦 Produto por Pedido
Essa entidade faz a relação entre produtos e pedidos, permitindo que cada pedido tenha múltiplos itens.

Pedido_idPedido: Identificador do pedido.
Produtos_idProdutos: Referência aos produtos incluídos.
Quantidade: Quantidade de cada produto em um pedido.
💳 Integração de Métodos de Pagamento
A maneira mais simples de integrar métodos de pagamento ao sistema é adicionar uma coluna MetodoPagamento na tabela Pedido, permitindo registrar facilmente o tipo de pagamento utilizado, como CartaoCredito, Pix, BoletoBancario, etc.

🛠️ Tecnologias Utilizadas
Modelagem: MySQL Workbench para a criação e visualização do esquema do banco de dados.
Banco de Dados: MySQL ou outro sistema de banco de dados relacional de sua escolha.
🚀 Como Usar
Importe o arquivo .mwb no MySQL Workbench para visualizar e modificar o esquema do banco de dados.
Utilize o esquema como base para criar o banco de dados em seu sistema de e-commerce.
Customize e expanda as funcionalidades conforme as necessidades do seu projeto.
