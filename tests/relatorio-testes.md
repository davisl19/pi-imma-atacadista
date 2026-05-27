# Relatório de Testes

Este documento apresenta os principais testes realizados no sistema IMMA Atacadista.

---

# Execução dos Testes

## Tipo de Teste

- Testes unitários
- Validação de interface
- Verificação de autenticação

## Tecnologia Utilizada

- Flutter Test

---

# Resultados dos Testes

| Caso | Objetivo | Resultado Esperado | Resultado Obtido | Status |
|---|---|---|---|---|
| CT01 | Cadastro válido | Cadastro realizado | Cadastro realizado | Aprovado |
| CT02 | Campos vazios | Mensagem de erro | Mensagem exibida | Aprovado |
| CT03 | E-mail inválido | Mensagem de erro | Mensagem exibida | Aprovado |
| CT04 | Cadastro duplicado | Bloqueio do cadastro | Bloqueio realizado | Aprovado |
| CT05 | Navegação login | goToLogin | goToLogin | Aprovado |
| CT06 | Login válido | goToHome | goToHome | Aprovado |
| CT07 | Login vazio | Mensagem de erro | Mensagem exibida | Aprovado |
| CT08 | Login inválido | Mensagem de erro | Mensagem exibida | Aprovado |

---

# Conclusão

Os testes realizados demonstraram que as funcionalidades principais do sistema estão operando corretamente dentro dos cenários planejados.

As validações de autenticação, cadastro e navegação apresentaram comportamento consistente e adequado aos requisitos definidos no projeto.
