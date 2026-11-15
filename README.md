# Banco de Dados de E-commerce

Projeto lógico de banco de dados relacional com clientes, produtos, pedidos, pagamentos, entregas, fornecedores, vendedores e estoques.

O diagrama foi gerado a partir das tabelas e chaves estrangeiras do script. As setas FK apontam da tabela dependente para a referenciada. O modelo editável do Workbench pode ser adicionado como `modelo-ecommerce.mwb`.

## Regras de negócio

- Uma conta é PF com CPF ou PJ com CNPJ, nunca ambos. Não há validação de dígitos verificadores.
- CPF, CNPJ e e-mail de cliente são únicos quando preenchidos.
- Um cliente pode cadastrar várias formas de pagamento.
- Cada pedido utiliza uma única forma cadastrada pelo próprio cliente, garantida por chave estrangeira composta.
- Um pedido pode ter no máximo uma entrega, com status e rastreio. O rastreio pode ser nulo antes da postagem.
- Produtos e fornecedores, produtos e estoques, e produtos e vendedores possuem relacionamentos de muitos para muitos, resolvidos por tabelas associativas.
- Um vendedor também pode ser fornecedor, identificado pela igualdade do CNPJ.
- O item de pedido preserva o preço praticado na compra.
- Quantidades e preços têm restrições para impedir valores inválidos.
