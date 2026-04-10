# ♿ Relatório de Auditoria: Tech Acessível

Este documento detalha a auditoria técnica de qualidade e acessibilidade realizada no portal **Tech Acessível**, utilizando a metodologia Lighthouse e inspeção manual de ativos.

## 📋 Informações Gerais
- **URL:** [techacessivel.info](https://techacessivel.info/)
- **Data do Teste:** 10 de Abril de 2026
- **Ferramentas:** Lighthouse (Chrome DevTools), Axe DevTools.
- **Dispositivo:** Mobile (Simulação Moto G Power)

---

## 📈 Resultados Lighthouse (Resumo)

| Categoria      | Nota | Status       |
|----------------|------|--------------|
| Performance    | 73   | ⚠️ Melhorar  |
| Acessibilidade | 100  | ✅ Excelente |
| Best Practices | 96   | ✅ Excelente |
| SEO            | 100  | ✅ Excelente |

> **Nota de Destaque:** O projeto atingiu a nota máxima em **Acessibilidade**, validando o propósito principal da plataforma em ser inclusiva.

---

## 🔍 Diagnóstico Técnico Detalhado

### 1. Performance (Oportunidades Críticas)
A nota de **73** deve-se principalmente ao tempo de carregamento do maior elemento da página (**LCP: 16.7s**).

* **Network Payload (Peso Total):** A página carrega **6,021 KiB** (aprox. 6MB), o que é excessivo para dispositivos móveis.
* **Ativos não otimizados:** * `Logoicone.png` (1,454 KiB) e `folder.png` (1,394 KiB) são os principais responsáveis pela lentidão.
    * `Cursos-online.png` (1,091 KiB) também apresenta peso fora dos padrões de performance web.
* **Scripts de Terceiros:** O *Google Tag Manager* entrega JavaScript não utilizado (economia estimada de 67 KiB).

### 2. Boas Práticas (Best Practices)
* **Aspect Ratio:** A imagem `logoprincipal.png` apresenta distorção (Aspect Ratio exibido de 1.85 vs. Original de 2.41).
* **Dimensões de Imagem:** Várias imagens de tutoriais (WhatsApp, Maps, Gmail) não possuem atributos `width` e `height` explícitos, o que pode causar instabilidade no layout durante o carregamento.

---

## 🛠️ Plano de Ação & Recomendações

Para elevar a performance para o **Green Score (90+)**, foram definidas as seguintes tarefas técnicas:

1.  **Conversão de Formatos:** Migrar todas as imagens `.png` para **`.webp`** ou **`.avif`**.
2.  **Compressão de Ativos:** Redimensionar o `Logoicone.png` e `folder.png` para as dimensões reais de exibição, reduzindo o peso em pelo menos 90%.
3.  **Refatoração HTML:** Adicionar atributos de largura e altura em todas as tags `<img>` para melhorar o CLS e as boas práticas.
4.  **Minificação:** Aplicar minificação no arquivo `style.css` para reduzir o tempo de parsing do CSS.

---

## 📸 Evidência Técnica
![Resultado Lighthouse](./lighthouse-techacessivel.png)

---
**Responsável:** Cleilton Silva  
*Engenharia de Software & QA*
