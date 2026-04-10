> **Projeto:** Auto IPE7 | **Versão:** 1.1 | **Data:** 10/04/2026 | **Responsável:** Cleilton Silva | **Status:** Finalizado
# Relatório de Testes e Auditoria de Qualidade - Auto IPE7

## 1. Visão Geral do Projeto
Este relatório documenta a fase de garantia de qualidade (QA) do site institucional **Auto IPE7**. O objetivo principal foi validar a experiência do utilizador em dispositivos móveis e a integridade das regras de negócio visuais, como o modo escuro persistente.

## 2. Escopo dos Testes
* **Funcionalidades:** Navegação entre seções, persistência do tema (Dark/Light Mode).
* **Não-Funcional:** Responsividade Mobile, Acessibilidade (WCAG) e Performance (Core Web Vitals).

## 3. Matriz de Execução
| Dispositivo | Navegador | Tipo de Teste | Resultado |
| :--- | :--- | :--- | :--- |
| Desktop (1920x1080) | Chrome | Funcional / UI | ✅ Passou |
| Mobile (iPhone SE) | Safari | Responsividade | ✅ Passou |
| Mobile (Pixel 7) | Chrome | Responsividade | ✅ Passou |

---

## 4. Evidências Técnicas

### A. Persistência de Dados (LocalStorage)
Foi validado que a escolha de tema do utilizador (Dark Mode) é salva localmente. Ao recarregar a página ou encerrar o navegador, o estado é mantido com 100% de sucesso, evitando o "flash" de luz indesejado.

### B. Auditoria Automatizada (Lighthouse)
O projeto apresenta altos índices de otimização, com os seguintes resultados obtidos na última auditoria:

* **Performance:** 97/100 
* **Acessibilidade:** 94/100 
* **Best Practices:** 100/100
* **SEO:** 100/100

> **Evidência Visual:**
> ![Status Lighthouse](lighthouse-autoipe7.png) 

---

## 5. Gestão de Defeitos (Bug Report)

### ✅ Defeitos Resolvidos
| ID | Título / Descrição | Severidade | Prioridade | Status |
| :--- | :--- | :--- | :--- | :--- |
| #001 | Sobreposição do menu mobile em ecrãs estreitos (Z-index). | **Alta** | **P1** | ✅ Corrigido |

**Passos para Reprodução (Bug #001):**
1. Aceder ao site via dispositivo mobile (ou simulação < 375px).
2. Acionar o menu hambúrguer.
3. **Resultado Obtido:** Itens do menu surgiam por baixo de elementos do cabeçalho.
4. **Resultado Esperado:** Menu deve sobrepor todos os elementos da interface.

---

### ⚠️ Defeitos em Backlog (Aguardando Manutenção)
| ID | Descrição | Elemento Afetado | Impacto | Severidade | Prioridade |
| :--- | :--- | :--- | :--- | :--- | :--- |
| #002 | Baixo contraste no texto. | `p.footer-copy.mt-3` | Dificulta leitura para utilizadores com baixa visão. | Média | P2 |
| #003 | Hierarquia de títulos incorreta. | `<h5>` "Mecânica Geral" | Prejudica navegação por leitores de ecrã e SEO. | Média | P2 |
| #004 | Ausência de Landmark Principal. | Tag `<main>` ausente | Falha na semântica; dificulta identificação do conteúdo. | Baixa | P3 |

---

## 6. Próximos Passos
As correções de backlog já foram mapeadas e serão aplicadas na próxima janela de manutenção do projeto, visando atingir o score de **100/100** em todos os pilares da auditoria.

---
*Relatório gerado por Cleilton Silva - Aspirante a QA Júnior.*
