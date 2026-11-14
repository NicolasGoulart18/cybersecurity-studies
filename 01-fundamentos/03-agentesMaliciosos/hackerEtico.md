# Hacker ético

Profissional que utiliza técnicas de hacking de forma autorizada para identificar vulnerabilidades e avaliar a segurança de uma organização, respeitando um escopo predefinido.

## 1. Papel e objetivos

Simula ataques e analisa sistemas para encontrar falhas técnicas, de processo, política ou configuração antes que agentes maliciosos as explorem.

Sua atuação ajuda a:

- Identificar vulnerabilidades e avaliar riscos.
- Analisar políticas, infraestrutura e controles.
- Apoiar auditorias e avaliações de segurança.
- Recomendar melhorias, como menor privilégio e Zero Trust.
- Reduzir a possibilidade de ataques e seus impactos.
- Proteger os dados e contribuir para a disponibilidade dos serviços.
- Elevar a maturidade de segurança da organização.

> O trabalho reduz riscos, mas não garante a ausência de ataques ou interrupções.

## 2. Escopo e limites

O escopo define o que está autorizado durante a avaliação:

- Sistemas, redes e aplicações que podem ser testados.
- Técnicas permitidas e atividades proibidas.
- Horários, duração e condições dos testes.
- Regras de acesso e uso dos recursos.
- Tratamento das informações coletadas.
- Procedimentos para interromper testes e comunicar incidentes.

O profissional deve seguir as regras acordadas, as boas práticas e as políticas, leis e padrões aplicáveis.

### Confidencialidade — NDA

O **NDA — Non-Disclosure Agreement** é um acordo de sigilo que pode ser exigido para proteger informações acessadas durante o trabalho.

> O NDA protege a confidencialidade, mas não substitui a autorização para realizar os testes.

### Limitações e riscos

Ultrapassar o escopo pode causar exposição de dados, alterações indevidas, interrupções e problemas legais.

Mesmo testes autorizados podem afetar ambientes despreparados e provocar **negação de serviço — DoS**. A classificação **DDoS** envolve múltiplas origens.

Por isso, os testes precisam ser planejados e ter limites claros.

## 3. Competências técnicas — Hard skills

- **Sistemas operacionais:** compreender seu funcionamento, especialmente Linux, incluindo terminal, permissões, processos e serviços.
- **Redes:** conhecer protocolos, endereçamento, portas e comunicação entre dispositivos.
- **Programação:** analisar código, adaptar ferramentas e desenvolver scripts de teste e exploração controlada.

## 4. Competências comportamentais — Soft skills

- Aprender continuamente e adaptar-se a novas tecnologias, como inteligência artificial.
- Analisar cenários criticamente e compreender ameaças emergentes.
- Agir com ética, responsabilidade e respeito à confidencialidade.
- Respeitar o escopo e as regras da organização.
- Comunicar descobertas, riscos e recomendações com clareza.

## 5. Persistência — Manutenção de acesso

Técnicas que permitem que um atacante tente manter ou recuperar o acesso ao sistema, inclusive após reinicializações. Conhecê-las ajuda o profissional de segurança a identificar falhas e recomendar controles.

- **Backdoors em aplicativos:** código inserido em servidores web ou aplicações internas que permite acesso remoto não autorizado. A continuidade após reiniciar depende de como foi implementado.
- **Tarefas agendadas:** uso do Agendador de Tarefas do Windows ou do `cron` no Linux para executar scripts periodicamente ou em eventos, como a inicialização, tentando restabelecer o acesso.
- **Scripts de inicialização:** alteração de arquivos executados automaticamente ao iniciar o sistema, aproveitando a confiança nesses mecanismos para carregar código malicioso.

Essas técnicas facilitam o retorno do atacante, mas podem deixar evidências detectáveis por monitoramento de integridade, análise de logs e ferramentas de proteção, como antivírus e **EDR — Endpoint Detection and Response**.