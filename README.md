# residencial-greenville

API para gestão de condomínios, projetada para atender aplicativo e portal web com foco em DDD, Clean Code e boas práticas.

## Visão da solução

- **Domínio principal**: gestão de unidades, moradores, reservas de áreas comuns, chamados, comunicados e cobranças.
- **Arquitetura sugerida (Clean Architecture + DDD)**:
  - `Domain`: entidades, value objects, regras de negócio e eventos de domínio.
  - `Application`: casos de uso, contratos de entrada/saída e orquestração.
  - `Infrastructure`: persistência, mensageria, provedores externos e autenticação.
  - `API`: controllers/endpoints HTTP, validação e serialização.

## Contrato inicial da API

O contrato inicial foi definido em `/openapi.yaml` com os principais recursos para o cenário multi-condomínio:

- Autenticação (`/auth/login`)
- Unidades (`/units`)
- Moradores (`/residents`)
- Reservas de áreas comuns (`/reservations`)
- Chamados de manutenção (`/maintenance-tickets`)
- Comunicados (`/notices`)
- Cobranças (`/charges`) e pagamentos (`/payments`)

## Próximos passos

1. Implementar os casos de uso com regras de domínio por agregado.
2. Definir estratégia de versionamento (`/v1`) e idempotência para operações críticas.
3. Adicionar testes automatizados por camada (unitários e integração).
