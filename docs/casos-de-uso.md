# Casos de Uso do Sistema

Este documento descreve os principais casos de uso do sistema, incluindo os fluxos de interação com o sistema e sua relação com os requisitos e funcionalidades do MVP.

---

## UC01 — Registrar Pedido por Voz
**Ator Principal:** Vendedor de Campo

**Objetivo:** Permitir que o vendedor registre pedidos utilizando voz durante visitas a clientes, evitando digitação manual.

**Pré-condições:**
- O vendedor deve estar autenticado no sistema.
- O cliente deve estar cadastrado.

**Pós-condições:**
- O pedido é registrado no sistema.
- Os dados do pedido são enviados para processamento.

**Fluxo Principal:**
1. O vendedor inicia a gravação de áudio no aplicativo.
2. O vendedor dita os produtos e quantidades solicitadas.
3. O sistema envia o áudio para processamento pela IA.
4. A IA converte o áudio em dados estruturados (JSON).
5. O sistema exibe o pedido para revisão.
6. O vendedor confirma o pedido.
7. O sistema registra o pedido no backend.

**Fluxos Alternativos:**
- **A1 — Falha na extração da IA:**
  - O sistema não consegue interpretar corretamente o áudio.
  - O sistema solicita revisão manual do pedido.
  - O vendedor corrige as informações antes de confirmar.

- **A2 — Falta de conexão com internet:**
  - O sistema detecta ausência de conexão.
  - O pedido é armazenado localmente.
  - O sistema sincroniza o pedido quando a conexão for restabelecida.

**Regras de Negócio:**
- RN01 — Cálculo de Comissão
- RN04 — Validação de Estoque

**Requisitos Relacionados:**
- RF01 — Captura multimodal (voz ou texto)
- RF02 — Extração automática via IA
- RNF02 — Disponibilidade offline

## Diagrama de Atividade
<img width="636" height="577" alt="image" src="https://github.com/user-attachments/assets/156d603f-9e6b-44de-9fb6-7872f2a32043" />

## Diagrama de Sequência
<img width="773" height="605" alt="image" src="https://github.com/user-attachments/assets/5d7762c5-b9db-48cd-b469-46898a3c0787" />



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

**Requisitos Relacionados:**
- RF03 — Gestão de recebíveis
- RNF03 — Segurança da informação

## Diagrama de Atividade

<img width="466" height="576" alt="image" src="https://github.com/user-attachments/assets/e2b48323-5762-4b07-815e-95baadf74e58" />

## Diagrama de Sequência

<img width="490" height="402" alt="image" src="https://github.com/user-attachments/assets/5826cf4e-ac3b-47b8-8f67-e9d6389ee8d1" />


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
- RN05 — Preço mínimo de venda

**Requisitos Relacionados:**
- RF06 — Integração com ERP
- RNF03 — Comunicação segura via HTTPS

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
- RF04 — Cálculo automático de comissão
- RNF04 — Usabilidade da interface

## Diagrama de Atividade

<img width="477" height="437" alt="image" src="https://github.com/user-attachments/assets/6719ed3f-827e-4d07-9556-016e43d5f185" />

## Diagrama de Sequência

<img width="537" height="527" alt="image" src="https://github.com/user-attachments/assets/ecb8483e-6596-401d-879c-f39f3133619d" />

---

# Relação com Funcionalidades do MVP

O **MVP (Produto Mínimo Viável)** do sistema será composto pelas funcionalidades essenciais para validar a proposta do projeto:

- Registro de pedidos por voz
- Revisão de pedidos gerados pela IA
- Registro digital de pagamentos
- Visualização de comissões do vendedor

Essas funcionalidades permitem validar o objetivo principal do sistema: **reduzir a digitação manual de pedidos e digitalizar o controle de recebíveis da IMMA Atacadista.**
