# CVE, CWE e CVSS

Esses padrões ajudam a identificar, classificar e avaliar vulnerabilidades.

| Padrão | Função |
| --- | --- |
| **CVE** | Identificar uma vulnerabilidade específica. |
| **CWE** | Classificar o tipo de fraqueza que pode originar vulnerabilidades. |
| **CVSS** | Avaliar a gravidade de uma vulnerabilidade. |

## CVE — Common Vulnerabilities and Exposures

Padroniza a identificação de vulnerabilidades publicamente divulgadas.

- Cada registro possui um identificador único.
- Formato: `CVE-AAAA-NNNN`, com quatro ou mais dígitos na parte numérica final.
- O registro reúne informações sobre a vulnerabilidade e referências.
- Ter um CVE não significa que a vulnerabilidade já foi explorada em ataques.

**Consulta:** [cve.org](https://www.cve.org/)

## CWE — Common Weakness Enumeration

É um catálogo de tipos de fraquezas em software e hardware que podem originar vulnerabilidades.

- Padroniza a descrição dessas fraquezas.
- Ajuda a identificar causas e prevenir falhas durante o desenvolvimento.
- Cada entrada possui um identificador, como `CWE-79`, relacionado a Cross-site Scripting (XSS).
- Uma mesma fraqueza pode estar associada a vários registros CVE.

**Consulta:** [cwe.mitre.org](https://cwe.mitre.org/)

## CVSS — Common Vulnerability Scoring System

É um sistema padronizado para avaliar a gravidade de vulnerabilidades.

- Produz uma pontuação de **0 a 10**.
- É mantido pela **FIRST — Forum of Incident Response and Security Teams**.
- Utiliza métricas sobre características da exploração e seus impactos.
- Essas métricas são representadas por uma sequência de texto chamada **vetor CVSS**.
- Ao registrar uma avaliação, é importante informar a versão, a pontuação e o vetor.

> O CVSS mede a gravidade técnica. Ele contribui para a análise de risco, mas não substitui essa análise.

**Calculadora oficial:** [first.org/cvss](https://www.first.org/cvss/calculator/4.0)

## Exemplo: XSS — Cross-site Scripting

XSS permite que scripts maliciosos, geralmente JavaScript, sejam executados no navegador da vítima no contexto de uma aplicação vulnerável.

Entre suas formas estão:

- **Refletido:** o conteúdo malicioso recebido é devolvido na resposta da aplicação.
- **Armazenado:** o conteúdo malicioso fica salvo e é apresentado posteriormente.
- **Baseado em DOM:** a falha ocorre na manipulação do conteúdo da página pelo código no navegador.

### Relação entre os padrões

- **CWE:** descreve o tipo de fraqueza relacionado ao XSS.
- **CVE:** identifica uma ocorrência específica da vulnerabilidade em um produto.
- **CVSS:** avalia a gravidade dessa ocorrência.

## Aplicação em um relatório

Ao analisar um CVE:

1. Verifique quais produtos e versões são afetados.
2. Confira a pontuação, a versão e o vetor CVSS.
3. Utilize as métricas ambientais para contextualizar a avaliação.
4. Considere também a exposição do sistema, sua importância e as evidências de exploração para priorizar a correção.