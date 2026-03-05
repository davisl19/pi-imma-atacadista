# Requisitos Não Funcionais (RNF)

**RNF01 — Desempenho**  
O tempo de processamento da IA (áudio para JSON) não deve ultrapassar 10 segundos em rede 4G.

**RNF02 — Disponibilidade**  
O aplicativo deve possuir um banco de dados local (SQLite) para permitir o registro de pedidos sem conexão com internet.

**RNF03 — Segurança**  
Toda comunicação entre o Flutter e o Backend Python deve ser criptografada via HTTPS/TLS.

**RNF04 — Usabilidade**  
A interface deve seguir as diretrizes do Material Design 3, com foco em botões grandes para uso em campo.

**RNF05 — Portabilidade**  
O sistema deve ser compatível com Android 10 ou superior.
