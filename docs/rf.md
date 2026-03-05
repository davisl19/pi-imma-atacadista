# Requisitos Funcionais (RF)

**RF01 — Captura Multimodal**  
O sistema deve permitir a entrada de pedidos via áudio (voz) e texto (linguagem natural).

**RF02 — Extração via IA**  
O backend (Gemini 1.5 Flash) deve converter a entrada bruta em um JSON estruturado com: SKU, Quantidade, Cliente e Condição de Pagamento.

**RF03 — Gestão de Malotes**  
O sistema deve permitir o registro digital de "Vales" (7, 14, 21 dias) e baixa de pagamentos, substituindo o caderno físico.

**RF04 — Cálculo de Comissão**  
O sistema deve calcular automaticamente 2,5% para vendas normais e 1,5% para produtos específicos (ex: promoções ou tabelas B).

**RF05 — Roteirização Logística**  
O sistema deve agrupar pedidos por cidade (Arceburgo, Itamogi, etc.) e gerar uma lista de carregamento para o estoque.

**RF06 — Integração ERP**  
O sistema deve enviar os dados validados para o banco de dados do TopGerente via API ou script de automação.
