# Regras de Negócio (RN)

**RN01 — Cálculo de Comissão**  
A comissão padrão é de 2,5%. Produtos em promoção ou tabelas especiais (Tabela B) possuem comissão reduzida de 1,5%.

**RN02 — Ciclo de Recebíveis**  
Os "Vales" permitidos para clientes de rota são estritamente de 7, 14, 21 ou até 28 dias corridos.

**RN03 — Bloqueio de Inadimplência**  
Clientes com Vales vencidos há mais de 5 dias no sistema devem ser sinalizados como "Bloqueados" para novos pedidos.

**RN04 — Validação de Estoque**  
Um pedido captado via IA só pode ser faturado se houver saldo positivo no ERP TopGerente. Caso contrário, entra como "Pendência".

**RN05 — Preço Mínimo**  
O sistema não deve permitir a venda de itens abaixo do preço de custo + impostos básicos (Margem de Segurança).
