# Agentes maliciosos e ataques de segurança

## 1. O que são agentes maliciosos?

São pessoas ou grupos que realizam ações intencionais para comprometer sistemas, redes, dispositivos ou informações.

Seus objetivos podem incluir ganho financeiro, espionagem, sabotagem, vingança ou causas políticas e ideológicas.

## 2. Motivos, objetivos e métodos

Para analisar um ataque, é importante diferenciar:

| Conceito | Significado | Exemplo |
| --- | --- | --- |
| **Motivação** | Por que o atacante realiza a ação. | Obter dinheiro. |
| **Objetivo** | O resultado que ele pretende alcançar. | Roubar dados de clientes. |
| **Método ou técnica** | Como ele executa a ação. | Phishing ou exploração de SQL Injection. |
| **Vulnerabilidade** | Fraqueza que pode ser explorada. | Falha na validação de entradas. |
| **Vetor de ataque** | Caminho utilizado para atingir o alvo. | E-mail malicioso ou aplicação exposta à internet. |

Os ataques podem explorar falhas em sistemas, configurações, processos, políticas e controles de segurança.

> Identificar IPs, portas e serviços faz parte do reconhecimento. Isso não significa, por si só, que uma vulnerabilidade foi explorada.

## 3. Ameaças e categorias de ataques

A lista abaixo reúne ameaças, técnicas, agentes e ambientes afetados. Nem todos os itens são vetores de ataque, e as categorias podem se sobrepor.

### 1. Ameaças em nuvem

Afetam dados, aplicações e serviços hospedados em ambientes de computação em nuvem.

Exemplos:

- Armazenamento exposto publicamente.
- Credenciais comprometidas.
- Permissões excessivas.
- Configurações inseguras.

Uma falha de isolamento pode afetar diferentes clientes, mas comprometer um cliente não significa automaticamente comprometer os demais.

### 2. APT — Advanced Persistent Threat

Significa **ameaça persistente avançada**.

Envolve adversários com conhecimento e recursos para manter presença no ambiente por longos períodos, adaptando suas ações às defesas.

Os objetivos podem incluir espionagem, roubo contínuo de informações ou sabotagem.

### 3. Vírus e worms

São tipos de **malware**, ou software malicioso.

- **Vírus:** infecta arquivos ou programas e depende da execução do conteúdo infectado para se ativar.
- **Worm:** consegue se propagar entre sistemas, geralmente pela rede, sem precisar infectar um programa hospedeiro.

A velocidade de propagação depende das condições do ambiente e das defesas existentes.

### 4. Ransomware

Malware que bloqueia o acesso a sistemas ou dados, frequentemente por meio de criptografia, e exige pagamento de resgate.

O ataque também pode envolver roubo de dados e ameaça de divulgação.

> Pagar o resgate não garante a recuperação dos arquivos.

### 5. Ameaças a dispositivos móveis

Afetam celulares e tablets.

Exemplos:

- Aplicativos maliciosos.
- Phishing por mensagens.
- Abuso de permissões.
- Exploração de sistemas desatualizados.

O nível de proteção depende do dispositivo, das configurações e de seu gerenciamento.

### 6. Botnet

Rede de dispositivos comprometidos que podem ser controlados por um atacante.

Pode ser utilizada para:

- Realizar ataques DDoS.
- Enviar spam.
- Distribuir malware.

### 7. Ameaças internas — Insider threats

Surgem de pessoas com acesso legítimo ao ambiente, como funcionários ou prestadores de serviço.

Podem envolver ações intencionais ou erros que causam danos.

**Exemplo de ataque interno:** um funcionário utiliza suas permissões para copiar e vender dados da empresa.

### 8. Phishing

Técnica de engenharia social que imita uma comunicação confiável para enganar a vítima.

Pode ocorrer por e-mail, SMS, mensagens ou páginas falsas.

Seus objetivos incluem roubar credenciais, obter informações ou induzir a instalação de malware.

### 9. Ameaças a aplicações web

Exploram fraquezas em sites e APIs.

Exemplos:

- XSS — Cross-site Scripting.
- SQL Injection.
- Falhas de autenticação e autorização.
- Sequestro de sessão.

### 10. Ameaças a dispositivos IoT

Afetam dispositivos conectados, como câmeras, sensores e equipamentos inteligentes.

Podem explorar senhas padrão, serviços expostos, firmware desatualizado e configurações inseguras.

### 11. Ataques ao sistema operacional

Exploram vulnerabilidades no sistema operacional ou em seus componentes.

Exemplos:

- Falhas de memória, como buffer overflow.
- Vulnerabilidades sem correção aplicada.
- Falhas que permitem elevação de privilégios.

### 12. Exploração de configurações inseguras

Também chamada de exploração de **security misconfigurations**.

Pode afetar servidores, aplicações, bancos de dados, redes e serviços em nuvem.

Exemplos:

- Contas e senhas padrão mantidas.
- Permissões excessivas.
- Serviços desnecessários habilitados.
- Mensagens de erro que expõem informações internas.

### 13. Ataques à camada de aplicação

Afetam funcionalidades e regras de uma aplicação, podendo permitir acesso indevido, roubo ou alteração de dados.

Exemplos:

- Injeção de comandos.
- Manipulação de regras de negócio.
- Falhas de controle de acesso.
- Negação de serviço na aplicação.

Essa categoria pode incluir ataques a aplicações web.

### 14. Ataques ao código e às dependências

Podem explorar erros de implementação, bibliotecas vulneráveis ou componentes comprometidos.

Exemplos:

- Uso de dependências com vulnerabilidades conhecidas.
- Inclusão de pacotes maliciosos.
- Alterações maliciosas no processo de distribuição de software.

Configurações padrão inseguras também podem gerar riscos, mas se enquadram principalmente em configurações inseguras.

## 4. DoS e DDoS

### DoS — Denial of Service

Ataque de **negação de serviço**: busca impedir ou prejudicar o acesso de usuários legítimos a um recurso.

### DDoS — Distributed Denial of Service

Ataque de **negação de serviço distribuída**, realizado a partir de múltiplas origens.

Pode sobrecarregar:

- A conexão de rede.
- Os equipamentos e protocolos de comunicação.
- Os recursos da aplicação.

Botnets podem ser utilizadas em DDoS, mas não são obrigatórias.

### Medidas de proteção

- Limitação de requisições — rate limiting.
- Monitoramento de tráfego e disponibilidade.
- Proteção especializada contra DDoS.
- Filtragem de tráfego com apoio do provedor.
- Uso adequado de cache e CDN.
- Plano de resposta a incidentes.

> Rate limiting ajuda em determinados ataques, mas não resolve sozinho todos os tipos de DDoS. Um ataque volumétrico pode saturar a conexão antes de alcançar a aplicação.