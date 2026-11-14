# Hash criptográfico

Função que transforma dados em um resumo de tamanho definido pelo algoritmo, semelhante a uma **impressão digital**.

## Características

- A mesma entrada produz o mesmo hash.
- Uma pequena alteração tende a modificar amplamente o resultado: **efeito avalanche**.
- Entradas diferentes podem produzir o mesmo hash: isso é uma **colisão**. Algoritmos seguros tornam difícil encontrar essas colisões.
- Não é criptografia reversível: não existe uma operação de “descriptografar o hash”.

## Integridade — exemplo da Petpark

Para verificar os dados de um agendamento:

1. Gerar e guardar um hash de referência.
2. Recalcular o hash posteriormente.
3. Comparar os resultados.

Hashes diferentes indicam alteração, que pode ser acidental ou maliciosa.

> O hash de referência precisa estar protegido. Se alguém modificar os dados e também substituir a referência, a comparação perde sua utilidade.

## Proteção de senhas

Senhas não devem ser armazenadas em texto puro.

- Utilizar uma função própria para senhas, como **Argon2id**, com um **salt único**.
- Armazenar o hash, o salt e os parâmetros necessários à verificação.
- No login, verificar a senha digitada usando esses dados.
- Se houver correspondência, a senha é validada; outros controles, como MFA, ainda podem ser exigidos.

**SHA-256 sozinho não é adequado para armazenar senhas**, pois permite testar muitas tentativas rapidamente.

> Hash serve para verificação, não para descriptografia. Porém, um atacante pode tentar descobrir uma senha fazendo suposições e verificando os resultados.
