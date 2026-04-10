# ♿ Relatório de Auditoria: Tech Acessível

Este documento detalha os testes de qualidade e acessibilidade realizados no portal Tech Acessível, garantindo conformidade com as diretrizes da WCAG 2.1.

## 📋 Informações Gerais
- **URL:** [techacessivel.info](https://techacessivel.info/)
- **Data do Teste:** Abril de 2026
- **Ambiente:** Chrome (Desktop), Safari (iOS), NVDA (Leitor de ecrã).

---

## 🔍 Escopo dos Testes

### 1. Navegação por Teclado (Acessibilidade Motora)
- [ ] Todos os elementos clicáveis recebem o foco (`outline`).
- [ ] Ordem de tabulação lógica e intuitiva.
- [ ] Ausência de "armadilhas de teclado" (Keyboard traps).

### 2. Contraste e Visual (Acessibilidade Visual)
- [ ] Taxa de contraste mínima de 4.5:1 para texto normal.
- [ ] Suporte a zoom de até 200% sem perda de conteúdo.
- [ ] Uso de cores não é o único meio de passar informação.

### 3. Semântica e Leitores de Ecrã
- [ ] Tags HTML5 semânticas (`<main>`, `<nav>`, `<article>`).
- [ ] Atributos `alt` presentes em todas as imagens informativas.
- [ ] Labels descritivos em todos os campos de formulário.

---

## 📈 Resultados Lighthouse (Acessibilidade)

| Categoria      | Nota | Status     |
|----------------|------|------------|
| Performance    | --   | Pendente   |
| Acessibilidade | --   | Pendente   |
| Boas Práticas  | --   | Pendente   |
| SEO            | --   | Pendente   |

---

## 📝 Notas de Implementação
*O foco atual é garantir que a navegação via leitor de ecrã (NVDA) descreva corretamente os cards de tecnologia.*

**Responsável:** Cleilton Silva
