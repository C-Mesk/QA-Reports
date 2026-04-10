# Relatório de Testes e Auditoria de Qualidade - Auto IPE7

## 1. Visão Geral do Projeto
Este relatório documenta a fase de garantia de qualidade (QA) do site institucional **Auto IPE7**. O objetivo principal foi validar a experiência do usuário em dispositivos móveis e a integridade das regras de negócio visuais.

## 2. Escopo dos Testes
- **Funcionalidades:** Navegação entre seções, persistência do tema claro/escuro.
- **Não-Funcional:** Responsividade, Acessibilidade (WCAG) e Performance.

## 3. Matriz de Execução
| Dispositivo | Navegador | Tipo de Teste | Resultado |
| :--- | :--- | :--- | :--- |
| Desktop (1920x1080) | Chrome | Funcional / UI | ✅ Passou |
| Mobile (iPhone SE) | Safari | Responsividade | ✅ Passou |
| Mobile (Pixel 7) | Chrome | Responsividade | ✅ Passou |

## 4. Evidências Técnicas
### A. Persistência de Dados (LocalStorage)
Foi validado que a escolha de tema do usuário (Dark Mode) é salva no navegador. Ao recarregar a página ou fechar o navegador, o estado é mantido com 100% de sucesso.

### B. Acessibilidade Técnica
Utilização do Lighthouse para auditoria, atingindo a marca de **100/100** em acessibilidade, garantindo contraste adequado e semântica correta para leitores de ecrã.

## 5. Gestão de Defeitos (Bugs)
- **ID #001:** Falha de sobreposição no menu mobile em ecrãs estreitos (Z-index).
- **Ação:** Correção aplicada no CSS para garantir visibilidade total dos itens.
- **Status:** Resolvido / Homologado.

---
*Relatório gerado por Cleilton Mesquita - Aspirante a QA Júnior.*
