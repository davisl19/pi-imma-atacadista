# Casos de Uso do Sistema

Este documento descreve os principais casos de uso do sistema, incluindo os fluxos de interação com o sistema e sua relação com os requisitos e funcionalidades do MVP.

<img width="620" height="427" alt="image" src="https://github.com/user-attachments/assets/45e5f5f7-a75a-4e45-a4ea-59a873740965" />

---

## UC01 — Receber Recomendações Inteligentes de Venda

**Ator Principal:** Vendedor de Campo

**Objetivo:** Permitir que o vendedor visualize recomendações inteligentes de produtos com base no desempenho de vendas, identificando itens com alta e baixa saída durante as visitas aos clientes.

### Pré-condições:
- O vendedor deve estar autenticado no sistema.
- O sistema deve possuir histórico de vendas registrado.

### Pós-condições:
- O vendedor recebe recomendações de produtos para oferecer ao cliente.
- O sistema apresenta informações sobre produtos com maior e menor desempenho de vendas.

### Fluxo Principal:
1. O vendedor acessa a tela inicial do aplicativo.
2. O vendedor seleciona a opção “Obter Recomendação por IA”.
3. O sistema consulta os dados de vendas registrados.
4. A IA analisa os produtos com maior e menor saída.
5. O sistema gera recomendações de venda.
6. O sistema exibe uma área de recomendações na parte inferior da tela.
7. O vendedor visualiza os produtos recomendados e utiliza as informações durante a negociação com o cliente.

### Fluxos Alternativos:

**A1 — Falha na análise da IA:**
- O sistema não consegue gerar recomendações no momento.
- O sistema informa indisponibilidade temporária das recomendações.

**A2 — Dados insuficientes para análise:**
- O sistema identifica ausência de histórico suficiente de vendas.
- O sistema informa que ainda não há dados suficientes para gerar recomendações.

### Regras de Negócio:
- RN01 — Cálculo de Comissão
- RN04 — Validação de Estoque

### Requisitos Relacionados:

- RF02 — Cálculo de comissão
- RF03 — Roteirização logística
- RF04 — Recomendações Inteligentes por IA
- RNF01 — Tempo de resposta

## Diagrama de Atividade

<img width="597" height="532" alt="image" src="https://github.com/user-attachments/assets/d2cbbaa1-d5eb-4a00-a07b-b46052d732d2" />

## Diagrama de Sequência

<img width="615" height="445" alt="image" src="https://github.com/user-attachments/assets/ecfa1742-1874-4688-ac00-9ea037dd4860" />

---

## UC02 — Registrar Baixa de Pagamento
**Ator Principal:** Conferente administrativo

**Objetivo:** Registrar digitalmente pagamentos recebidos dos clientes nas rotas de venda.

**Pré-condições:**
- O pedido deve estar registrado no sistema.

**Pós-condições:**
- O sistema atualiza o status do pedido para pago.

**Fluxo Principal:**
1. O conferente acessa o módulo de gestão de recebíveis.
2. O sistema exibe pedidos pendentes de pagamento.
3. O conferente seleciona um pedido.
4. O conferente registra o pagamento recebido.
5. O sistema atualiza o status do pedido.

**Fluxos Alternativos:**
- **A1 — Vale vencido:**
  - O sistema detecta que o prazo do vale foi ultrapassado.
  - O sistema alerta o gestor sobre inadimplência.

**Regras de Negócio:**
- RN02 — Ciclo de Recebíveis
- RN03 — Bloqueio de Inadimplência

## Diagrama de Atividade

<img width="430" height="422" alt="image" src="https://github.com/user-attachments/assets/d762fada-c659-4c40-a3f6-55c327f1be27" />


## Diagrama de Sequência

<img width="700" height="543" alt="image" src="https://github.com/user-attachments/assets/026f9c6c-5e45-421d-bb0c-8b1db5aa59be" />

---

## UC03 — Sincronizar Pedidos com o ERP
**Ator Principal:** Sistema (Backend)

**Objetivo:** Enviar automaticamente pedidos registrados no aplicativo para o ERP TopGerente.

**Pré-condições:**
- O pedido deve estar confirmado no sistema.
- A integração com o ERP deve estar ativa.

**Pós-condições:**
- O pedido é registrado no ERP.

**Fluxo Principal:**
1. O sistema identifica pedidos confirmados pelos vendedores.
2. O backend organiza os dados do pedido no formato esperado pelo ERP.
3. O sistema envia os dados para o ERP TopGerente.
4. O ERP registra o pedido no banco de dados.
5. O sistema atualiza o status do pedido como sincronizado.

**Fluxos Alternativos:**
- **A1 — Falha na comunicação com o ERP:**
  - O sistema detecta erro na integração.
  - O pedido é marcado como pendente de sincronização.
  - O sistema tenta reenviar automaticamente posteriormente.

**Regras de Negócio:**
- RN04 — Validação de Estoque

## Diagrama de Atividade

<img width="368" height="646" alt="image" src="https://github.com/user-attachments/assets/4a18ca28-5271-43d2-acbf-d1755cde0d79" />

## Diagrama de Sequência

<img width="395" height="467" alt="image" src="https://github.com/user-attachments/assets/6471a371-4780-41d7-bac4-7ae92a5cf979" />

---

## UC04 — Visualizar Comissões do Vendedor
**Ator Principal:** Vendedor

**Objetivo:** Permitir que o vendedor acompanhe suas comissões acumuladas no período.

**Pré-condições:**
- O vendedor deve estar autenticado.
- O sistema deve possuir registros de vendas do vendedor.

**Pós-condições:**
- O vendedor visualiza o total de comissões acumuladas.

**Fluxo Principal:**
1. O vendedor acessa o dashboard do sistema.
2. O sistema consulta os pedidos registrados pelo vendedor.
3. O sistema calcula automaticamente as comissões.
4. O sistema exibe o valor total de comissão do mês.

**Fluxos Alternativos:**
- **A1 — Nenhuma venda registrada:**
  - O sistema identifica que não há vendas no período.
  - O sistema exibe comissão igual a zero.

**Regras de Negócio:**
- RN01 — Cálculo de Comissão

**Requisitos Relacionados:**
- RF02 — Cálculo de comissão
- RNF04 — Usabilidade da interface

## Diagrama de Atividade

<img width="477" height="437" alt="image" src="https://github.com/user-attachments/assets/6719ed3f-827e-4d07-9556-016e43d5f185" />

## Diagrama de Sequência

<img width="537" height="527" alt="image" src="https://github.com/user-attachments/assets/ecb8483e-6596-401d-879c-f39f3133619d" />

---

# Relação com Funcionalidades do MVP

O **MVP (Produto Mínimo Viável)** do sistema será composto pelas funcionalidades essenciais para validar a proposta do projeto:

- Recomendações inteligentes por IA
- Registro digital de pagamentos
- Visualização de comissões do vendedor

Essas funcionalidades permitem validar o objetivo principal do sistema: **reduzir a digitação manual de pedidos e digitalizar o controle de recebíveis da IMMA Atacadista.**
