# Controle de segurança
    Ajuda minimizar riscos de segurança para os ativos

    Metodos tecnicos e nao tecnicos(tecnico pode ser código e não tecnico pode ser um cadeado)

    Controles sao categorizados de acordo com a função 

### Objetivo do controle de segurança
    -  Redeuzem o risco de segurança
    - Proteguem ativos contra ameaças

### Tipos de controle
    - Tecnicos ou logicos
    - Adminstrativos
    - Fisicos

### Controles de segurança (entendendo)
    - Criterios de seleção
        - Baseados no valor do ativo
        - Evitam gastar com ativos de pouco valor

    - Fatores do valor do ativo
        - Custo de substituição

### Classificação dos controles de segurança
    -Preventivo: 
        -Detectar problemas antes que surjam
        - Monitorar operções e as entradas.
        - Prever problemas e ajustar.Evitar erros ou atos maliciosos.
    - Detectivo
        - Detectar e relatar a ocorrencia do erro,omissao ou ato malicioso
    - Corretivo
        - Minimizar o impacto da ameaça
        - Corrigir os probçemas detectados
        - Corrigir os erros decorrentes de falhas
    - Dissuasivo 
        - Reduzir a probabilidade de uma violação

 Preventivo: O foco principal é evitar que um risco seja explorado e se transforme em uma vulnerabilidade. O objetivo é impedir que atos maliciosos ou erros aconteçam. Um exemplo citado na aula é o uso de um WAF ou configurações específicas para evitar XSS.

Detectivo: Sua função é identificar a ocorrência de algo antes que o impacto se concretize ou para alertar que uma tentativa de ataque está acontecendo. Ele serve para sinalizar que o ambiente está sob ameaça.

Corretivo: Este entra em cena quando o risco já foi identificado ou a vulnerabilidade já existe. O objetivo aqui é reparar o problema e reduzir os danos ou eliminar a brecha encontrada.

Dissuasivo: Este controle atua na psicologia do atacante, reduzindo a probabilidade de ele tentar explorar o risco. Ele cria barreiras ou avisos que desencorajam o invasor de prosseguir com o ataque.                             # Controles de segurança

Medidas que ajudam a **reduzir riscos e proteger ativos contra ameaças**. Podem ser técnicas ou não técnicas, como uma validação no código ou um cadeado.

## Tipos de controle

- **Técnicos ou lógicos:** implementados em sistemas, como autenticação, firewalls e validações no código.
- **Administrativos:** políticas, procedimentos e treinamentos.
- **Físicos:** protegem o acesso físico, como cadeados, portas e catracas.

## Critérios de seleção

Os controles devem considerar o **valor do ativo, os riscos e o custo da proteção**. O investimento precisa ser proporcional ao que se deseja proteger.

O valor do ativo envolve fatores como:
- Custo de substituição.
- Importância para a operação.
- Impacto da perda, alteração ou exposição das informações.

## Classificação por função

### Preventivo

Busca **impedir que erros ou ataques aconteçam**, reduzindo a possibilidade de exploração de vulnerabilidades.

- Atua antes do incidente.
- Inclui restrições de acesso, validação de entradas e configurações seguras.
- **Exemplo:** um WAF pode ajudar a bloquear tentativas de XSS.

### Detectivo

Busca **identificar e relatar erros, omissões ou atividades maliciosas**, durante ou após sua ocorrência.

- Monitora operações e sinaliza comportamentos suspeitos.
- **Exemplo:** um sistema que gera alertas sobre tentativas de acesso indevido.

### Corretivo

Busca **corrigir problemas detectados e reduzir os danos de um incidente**.

- Corrige falhas e suas consequências.
- Ajuda a restaurar o funcionamento do ambiente.
- **Exemplo:** aplicar uma atualização para corrigir uma vulnerabilidade.

### Dissuasivo

Busca **desencorajar tentativas de violação**, influenciando a decisão de quem pretende atacar.

- Reduz a probabilidade de uma tentativa.
- **Exemplo:** avisos de monitoramento e de responsabilização por acessos indevidos.

> Um mesmo controle pode cumprir mais de uma função.