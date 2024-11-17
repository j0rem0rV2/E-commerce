Projeto de Banco de Dados de E-commerce
Este projeto é um esquema de banco de dados para um sistema de e-commerce que gerencia clientes, produtos, pedidos, entregas e fornecedores. O objetivo é fornecer uma estrutura clara e eficiente para gerenciar operações de comércio eletrônico, incluindo o processamento de pedidos e a rastreabilidade de entregas.

Estrutura do Banco de Dados
O modelo de dados inclui as seguintes principais entidades:

1. Cliente
idCliente: Identificador único do cliente.
Nome: Nome do cliente.
Endereço: Endereço de entrega do cliente.
Pagamento: Método de pagamento utilizado pelo cliente.
2. Pessoa Física e Pessoa Jurídica
Pessoa Física: Informações adicionais para clientes individuais, incluindo CPF.
Pessoa Jurídica: Informações adicionais para clientes empresariais, incluindo CNPJ.
3. Pedido
idPedido: Identificador único do pedido.
Compra: Detalhes sobre os produtos comprados.
Endereço: Endereço de entrega associado ao pedido.
Status da Entrega: Indica o estado da entrega do pedido.
Frete: Custo de entrega associado ao pedido.
4. Entrega
Entregador_idEntregador: Identificador do entregador responsável.
Pedido_idPedido: Referência ao pedido correspondente.
Status de entrega: Estado atual da entrega (ex.: "Pendente", "Em transporte", "Entregue").
Código de Rastreamento: Código para rastrear a entrega.
5. Produtos e Estoque
Produtos: Informações sobre produtos disponíveis para venda, incluindo categoria, descrição e valor.
Produtos_has_Estoque: Tabela que relaciona produtos ao estoque e quantidade disponível.
6. Fornecimento
Fornecedor_idFornecedor: Identificador do fornecedor.
Produtos_idProdutos: Referência aos produtos fornecidos por um fornecedor específico.
7. Produto por Pedido
Pedido_idPedido: Identificador do pedido.
Produtos_idProdutos: Referência aos produtos incluídos no pedido.
Quantidade: Quantidade de cada produto no pedido.
Requisitos de Pagamento
A forma mais simples de integrar métodos de pagamento neste sistema é adicionar uma coluna MetodoPagamento na tabela Pedido, permitindo registrar o tipo de pagamento (ex.: CartaoCredito, Pix, BoletoBancario).

Tecnologias Utilizadas
Modelagem: MySQL Workbench para criação do esquema de banco de dados.
Banco de Dados: MySQL ou outro sistema de banco de dados relacional.
