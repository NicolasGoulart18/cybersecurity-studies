# Reconhecimento e fases do hacking

## 1. Reconhecimento

Coleta de informações sobre o alvo para compreender seu ambiente e identificar possíveis superfícies de ataque.

### Passivo

Obtém informações sem interagir diretamente com a infraestrutura do alvo.

**Exemplos:** pesquisas em fontes públicas, mecanismos de busca e bases de dados de terceiros.

### Ativo

Obtém informações por meio de interação direta com o alvo.

**Exemplos:** varreduras de portas, requisições ao servidor e contato telefônico para coletar informações.

> Uma ligação pode envolver engenharia social, dependendo da abordagem utilizada.

### Ferramentas e técnicas

| Recurso | Uso |
| --- | --- |
| **Google Hacking — Google Dorking** | Utiliza operadores de busca para localizar informações indexadas pelo Google. |
| **Shodan** | Permite consultar informações sobre dispositivos e serviços conectados à internet. Consultar dados já coletados é reconhecimento passivo em relação ao alvo. |
| **DIRB** | Busca caminhos, arquivos e diretórios em aplicações web por meio de requisições. É uma ferramenta de reconhecimento ativo. |

## 2. Scanning — Varredura

Identifica hosts, portas e serviços acessíveis para aprofundar o conhecimento sobre o ambiente.

### Identificação de portas e serviços

Ferramentas como o **Nmap** verificam quais portas estão abertas e quais serviços podem estar disponíveis.

**Exemplo:** a porta `22/TCP` é normalmente associada ao SSH, mas estar aberta não comprova que o serviço seja SSH. É necessário identificá-lo.

Uma porta aberta representa um possível ponto de interação, não necessariamente uma vulnerabilidade.

### Identificação de versões

Busca identificar a versão do software em execução, como um servidor MySQL.

Isso permite pesquisar CVEs e verificar se alguma falha conhecida se aplica ao ambiente — como identificar o modelo de uma fechadura antes de pesquisar suas características.

> A versão identificada é uma pista, não uma confirmação de vulnerabilidade: correções e configurações também precisam ser verificadas.

### Enumeração

Aprofunda a coleta de informações sobre serviços, recursos, usuários e configurações.

O Nmap possui scripts para diferentes verificações. Por exemplo, `mysql-enum` tenta enumerar usuários válidos em determinadas condições do MySQL.

> O `mysql-enum` é classificado como intrusivo e não corresponde apenas à consulta da versão do serviço.

### Ferramentas

- **Nmap:** ferramenta gratuita e de código aberto para descoberta de hosts, varredura de portas, identificação de serviços e auditoria de segurança.
- **Metasploit Framework:** plataforma de código aberto para pentest, desenvolvimento de módulos, exploração e validação de vulnerabilidades.
- **Metasploit Pro:** edição comercial da plataforma Metasploit.

## 3. Manutenção de acesso

Após comprometer um sistema, um atacante pode tentar estabelecer persistência para acessá-lo novamente.

- Pode utilizar backdoors, rootkits ou trojans com funções de acesso remoto.
- Pode alterar dados, contas e configurações.
- A persistência depende da técnica utilizada e dos privilégios obtidos.

## 4. Ocultação de rastros

Tentativa de esconder atividades maliciosas e dificultar sua identificação.

Pode envolver adulteração ou exclusão de registros e alterações nos sistemas comprometidos.

> Ocultar rastros e manter acesso são objetivos diferentes, embora possam ocorrer juntos. Alterar registros locais não elimina necessariamente evidências armazenadas em outros sistemas.

### Logs no Linux

- **`/var/log/`:** diretório que reúne diversos arquivos de log. O caminho correto não é `/var/logs`.
- **`/var/log/auth.log`:** pode registrar autenticações, acessos SSH e uso de `sudo` em sistemas Debian/Ubuntu.

A existência e a localização desses registros dependem da distribuição e da configuração. Alguns eventos também podem estar no journal do systemd.