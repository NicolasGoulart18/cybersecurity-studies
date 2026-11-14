# Controles de segurança

Medidas técnicas ou não técnicas que ajudam a **reduzir riscos e proteger ativos contra ameaças**, como uma validação no código ou um cadeado. Os controles podem ser classificados pelo tipo e pela função.

**Palavras-chave:** proteção, ativos, redução de riscos.

## Tipos de controle

| Tipo | O que envolve | Exemplos | Palavras-chave |
|---|---|---|---|
| **Técnico ou lógico** | Medidas implementadas em sistemas. | Autenticação, firewall e validação de entradas. | Sistemas, código, acesso lógico. |
| **Administrativo** | Regras e orientações para pessoas e processos. | Políticas, procedimentos e treinamentos. | Regras, pessoas, processos. |
| **Físico** | Proteção do espaço e do acesso aos equipamentos. | Cadeados, portas e catracas. | Ambiente, barreiras, acesso físico. |

## Critérios de seleção

A escolha deve considerar o **valor do ativo, os riscos e o custo da proteção**. O investimento precisa ser proporcional ao que se deseja proteger.

O valor do ativo envolve:

- **Custo de substituição:** quanto custa repor o ativo.
- **Importância operacional:** quanto a organização depende dele.
- **Impacto nas informações:** consequências da perda, alteração ou exposição dos dados.

**Palavras-chave:** valor, risco, impacto, custo-benefício.

## Classificação por função

### Preventivo — impedir

Busca **evitar erros e ataques**, reduzindo a possibilidade de exploração de vulnerabilidades.

- Atua antes do incidente, com restrições de acesso, validação de entradas e configurações seguras.
- **Exemplo:** um WAF pode ajudar a bloquear tentativas de XSS.

**Palavras-chave:** impedir, evitar, bloquear.

### Detectivo — identificar

Busca **identificar e relatar erros, omissões ou atividades maliciosas**, durante ou após sua ocorrência.

- Monitora operações e sinaliza comportamentos suspeitos.
- **Exemplo:** um sistema que alerta sobre tentativas de acesso indevido.

**Palavras-chave:** identificar, monitorar, alertar.

### Corretivo — corrigir

Busca **corrigir problemas detectados e reduzir os danos**, tratando falhas e suas consequências.

- Ajuda a restaurar o funcionamento do ambiente.
- **Exemplo:** aplicar uma atualização para corrigir uma vulnerabilidade.

**Palavras-chave:** corrigir, reparar, reduzir danos.

### Dissuasivo — desencorajar

Busca **desencorajar tentativas de violação**, influenciando a decisão de quem pretende atacar.

- **Exemplo:** avisos de monitoramento e de responsabilização por acessos indevidos.

**Palavras-chave:** desencorajar, avisar, inibir.

## Para lembrar

- **Tipo:** como o controle é implementado — técnico, administrativo ou físico.
- **Função:** para que ele serve — impedir, identificar, corrigir ou desencorajar.
- **Um mesmo controle pode ter mais de uma função:** um firewall pode bloquear conexões (preventivo) e gerar alertas (detectivo).
- **Reduzir riscos não significa eliminar todos eles:** o risco que permanece é chamado de risco residual.
