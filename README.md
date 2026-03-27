# PI-IMMA-ATACADISTA 
> *Transformação Digital e IA Generativa aplicada à logística e vendas da IMMA Atacadista.*

 Desenvolvido como projeto integrador para o curso de Ciência da Computação (UNIFEOB). O sistema utiliza Inteligência Artificial para eliminar processos manuais, otimizar rotas logísticas e digitalizar a gestão financeira de uma operação atacadista real.

---

## Visão Geral
A *IMMA Atacadista*, em Arceburgo (MG), opera hoje com fluxos 100% analógicos. O sistema surge para atuar como uma camada inteligente sobre o ERP TopGerente, convertendo interações em linguagem natural (voz/texto) em dados estruturados, eliminando o erro humano e o uso extensivo de papel.

### O Problema
* *Gargalo de Digitação:* 45 minutos perdidos por rota na transcrição de pedidos manuais.
* *Gestão "No Caderno":* Controle de recebíveis (vales de 7, 14, 21 dias) sem rastro digital.
* *Latência Logística:* Dificuldade em agrupar pedidos para carregamento imediato.

### Objetivos
1. *Automação de Pedidos:* Extração multimodal via *Gemini 1.5 Flash*.
2. *Logística D+1:* Roteirização automática por cidade.
3. *Paperless:* Digitalização total do controle de malotes e comissões.

---

## Tecnologias Utilizadas
* *Frontend:* Flutter (Mobile) - Foco em usabilidade de campo.
* *Backend:* Python & FastAPI - Orquestração e lógica de negócio.
* *IA:* Google Gemini API - Processamento de linguagem natural e visão.
* *Banco de Dados:* SQLite (Local) e Integração via API (ERP).

---

## Estrutura do Repositório

* */docs*: Documentação técnica completa.
    * [Regras de Negócio (RN)](./docs/rn.md)
    * [Requisitos Funcionais (RF)](./docs/rf.md)
    * [Requisitos Não Funcionais (RNF)](./docs/rnf.md)
    * [Backlog Inicial](./docs/backlog-inicial.md)
    * [Casos de Uso](./docs/casos-de-uso.md)
* */mobile*: Código-fonte do aplicativo em Flutter.
* */backend*: Scripts de integração e orquestração da IA.
* */assets: Identidade visual e o **Vídeo de Sustentabilidade*.

---

## Sustentabilidade (ODS 12)
O projeto está diretamente alinhado ao *ODS 12 - Consumo e Produção Responsáveis*. Através da eliminação de formulários físicos e otimização de rotas de entrega, reduzimos o desperdício de papel e a emissão de carbono na logística regional.

---

## Equipe (UNIFEOB)
* *Eduardo Ferreira Honório*
* *Davi Souza Lima*
* *Gabriel Novais Corsini*
* *Eduardo Rodrigues dos Santos*
* *Eduardo Carvalho Celeghini Barbosa*

---
Este projeto é uma iniciativa acadêmica em parceria com a IMMA Atacadista.

