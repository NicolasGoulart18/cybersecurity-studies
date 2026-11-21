# Defesa em profundidade — Segurança em camadas

[Voltar ao índice de fundamentos](../README.md)

> **Tipo:** anotação teórica | **Assunto:** controles de segurança e resposta a incidentes  
> **Origem:** resumo da aula sobre segurança em camadas. Este arquivo não representa um laboratório realizado.

## 1. O que é defesa em profundidade?

**Defesa em profundidade (Defense in Depth)** é uma estratégia que utiliza **múltiplas camadas de proteção complementares** para reduzir a probabilidade de um ataque bem-sucedido e limitar seus impactos.

**Ideia principal:** não depender de uma única barreira. Se um controle falhar, outros podem continuar prevenindo, detectando ou contendo a ameaça.

- **Superfície de ataque:** conjunto de pontos que um invasor poderia tentar explorar, como serviços expostos, portas, APIs, contas e funcionalidades.
- **Redução da superfície de ataque:** remover serviços desnecessários, corrigir configurações inseguras e restringir acessos.
- **Defesa em camadas:** aplicar controles em diferentes partes do ambiente, mesmo quando nem todos os riscos podem ser eliminados.

> Ter várias camadas **não significa** que um atacante precise atravessá-las em ordem. Uma falha na aplicação, por exemplo, pode ser explorada diretamente pela internet. As proteções devem ser independentes e complementares sempre que possível.

## 2. Principais camadas e exemplos

| Camada | O que é protegido | Exemplos de controles |
| --- | --- | --- |
| **Física** | Instalações, servidores e equipamentos | Trancas, cercas, câmeras e controle de entrada. |
| **Perímetro e rede** | Conexões e comunicação entre sistemas | Firewall, ACLs (listas de controle de acesso), segmentação, IDS/IPS e proteção contra DDoS. |
| **Host (servidor ou dispositivo)** | Sistema operacional e programas instalados | Atualizações de segurança, antivírus/EDR, permissões mínimas e configuração segura. |
| **Aplicação** | Funcionalidades e regras de negócio | Autenticação e autorização, validação de entradas, tratamento seguro de saídas e WAF. |
| **Dados** | Informações armazenadas e processadas | Controle de acesso, criptografia em repouso, backups e exclusão segura. |
| **Pessoas e processos** | Identidades, decisões e operações | MFA, treinamento contra phishing, políticas de acesso e procedimentos de resposta. |

**Dados em trânsito:** protocolos como **TLS** ajudam a proteger a confidencialidade e a integridade da comunicação. Eles não impedem, por si só, ataques como SQL Injection, XSS ou DDoS.

## 3. Funções dos controles de segurança

As funções abaixo podem atuar em **mais de uma camada**:

| Função | Objetivo | Exemplos |
| --- | --- | --- |
| **Preventiva** | Impedir ou dificultar uma ação indevida. | Firewall, MFA, correções de software e validações seguras. |
| **Detectiva** | Identificar e alertar sobre eventos suspeitos. | IDS, monitoramento, análise de logs e alertas. |
| **Corretiva e de recuperação** | Corrigir falhas e restaurar serviços ou dados. | Atualizações corretivas, restauração de backup e plano de recuperação. |
| **Dissuasiva** | Desencorajar tentativas de violação. | Avisos de monitoramento, presença de vigilantes e sinalização. |

Um mesmo recurso pode desempenhar mais de uma função. Por exemplo, uma câmera pode **dissuadir** e também ajudar a **detectar** uma ocorrência.

Para revisar a classificação, consulte [controles de segurança](controlesDeSeguranca.md) e [controles dissuasivos, detectivos e preventivos](dissuasivo.md).

## 4. Eventos, incidentes e resposta

- **Evento de segurança:** ocorrência observável em um sistema ou rede. Nem todo evento é um incidente.
- **Incidente de segurança:** ocorrência que compromete ou ameaça comprometer a confidencialidade, integridade ou disponibilidade, conforme os critérios adotados pela organização.
- **Sala de guerra (war room):** reunião ou canal de coordenação entre as equipes durante um incidente importante. É uma forma de organizar a resposta, não uma camada técnica de proteção.

### Etapas comuns da resposta a incidentes

1. **Preparação:** definir responsáveis, procedimentos, ferramentas, comunicação e planos de contingência.
2. **Detecção e análise:** identificar alertas, investigar evidências e avaliar o alcance do incidente.
3. **Contenção:** limitar a propagação ou o impacto, como isolar um servidor comprometido.
4. **Erradicação:** remover a causa do comprometimento e corrigir falhas exploradas.
5. **Recuperação:** restaurar serviços e dados com segurança e acompanhar possíveis recorrências.
6. **Lições aprendidas:** revisar o ocorrido e melhorar controles, monitoramento e procedimentos.

> A ordem pode variar e algumas etapas podem acontecer em paralelo, dependendo do incidente.

## 5. Backup, redundância e recuperação de desastres

- **Backup:** cópia de dados que pode ser usada para recuperação após exclusão, corrupção ou indisponibilidade.
- **Redundância:** recursos adicionais que ajudam a manter serviços disponíveis em caso de falha.
- **Balanceamento de carga:** distribui requisições entre recursos disponíveis para melhorar desempenho e disponibilidade.
- **Disaster Recovery (DR):** plano e procedimentos para recuperar sistemas e operações após uma interrupção grave.

**Atenções importantes:**

- Um backup pode recuperar dados apagados ou corrompidos, mas **não desfaz um vazamento** de informações já copiadas por um atacante.
- Redundância e balanceamento podem aumentar a disponibilidade, mas **não substituem** soluções específicas contra ataques DDoS, como filtragem de tráfego e serviços de mitigação.
- Backups devem ser protegidos e ter sua restauração testada periodicamente.

## 6. Exemplo prático de raciocínio: aplicação web

Imagine uma aplicação exposta à internet:

1. **Rede:** firewalls restringem acessos indevidos; TLS protege os dados durante o transporte.
2. **Host:** atualizações e permissões reduzidas dificultam o comprometimento do servidor.
3. **Aplicação:** consultas parametrizadas ajudam a impedir SQL Injection; codificação de saída conforme o contexto ajuda a prevenir XSS.
4. **Proteção adicional:** um **WAF (Web Application Firewall)** pode identificar e bloquear algumas requisições maliciosas.
5. **Detecção:** logs, métricas e alertas ajudam a identificar comportamentos suspeitos.
6. **Dados e continuidade:** permissões, criptografia e backups ajudam a limitar impactos e recuperar informações quando necessário.

### Caso de XSS

Se um atacante tentar inserir um script em uma página:

- A **prevenção principal** está no desenvolvimento seguro, especialmente na codificação de saída e no tratamento adequado de conteúdo não confiável.
- O **WAF** funciona como uma defesa adicional, mas não garante bloquear todos os tipos de XSS. Procurar apenas caracteres especiais é insuficiente.
- A **detecção** pode envolver logs, alertas e investigação de comportamento inesperado.
- A **resposta** envolve corrigir a vulnerabilidade, avaliar impactos e monitorar o ambiente.

> Segurança em camadas não substitui o desenvolvimento seguro da aplicação. Ela reduz a dependência de um único controle.

## 7. Resumo para revisão

- **Defesa em profundidade = várias proteções complementares**, não uma barreira única.
- **Superfície de ataque = possíveis pontos de exploração**; minimizá-la é uma estratégia importante.
- **Camadas = física, rede, host, aplicação, dados, pessoas e processos.**
- **Controles = preventivos, detectivos, corretivos e dissuasivos.**
- **Resposta a incidentes = preparar, detectar, conter, erradicar, recuperar e aprender.**
- **Backup não impede vazamentos; TLS não impede injeções; WAF não substitui código seguro.**
- Mesmo com várias proteções, permanece um **risco residual**, que precisa ser acompanhado.

## Relação com outros estudos

- [Princípios da segurança da informação](../01-SegurancaInformacao/principios-seguranca-informacao.md)
- [Ameaças, vulnerabilidades e riscos](../02-AmeacasCiberneticas/ameacas%26riscos.md)
- [Controles de segurança](controlesDeSeguranca.md)
