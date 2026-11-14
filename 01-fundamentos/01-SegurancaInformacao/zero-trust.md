# Zero Trust

Modelo de segurança que não concede confiança automática a usuários ou dispositivos apenas por estarem dentro da rede ou pertencerem à empresa.

## Verificação contínua e segmentação

O acesso é avaliado conforme o contexto, podendo considerar:

- Identidade, permissões e autenticação multifator.
- Estado de segurança do dispositivo.
- Comportamento do usuário.
- Sensibilidade do recurso e risco da solicitação.

As permissões devem seguir o **menor privilégio**, com reavaliação do acesso conforme necessário.

A segmentação de redes e recursos ajuda a limitar a movimentação do atacante e os danos de um comprometimento.

> Verificação contínua não significa pedir senha ou MFA a cada clique.

## Implementação e desafios

Exige mudanças técnicas e culturais, conhecimento dos ativos e controles granulares.

- **Vantagens:** reduzir acessos indevidos e limitar danos em caso de invasão.
- **Desafios:** integrar sistemas legados, administrar a complexidade e manter monitoramento contínuo de comportamentos anômalos.
