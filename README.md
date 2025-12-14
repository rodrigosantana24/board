# Board

Aplicação Java para gerenciar um quadro com colunas e cards. O projeto é uma aplicação de console que aplica migrações de banco via Liquibase e inicia um menu interativo para operar sobre entidades (boards, colunas, cards).

**Principais características:**
- Migrações de banco com Liquibase 
- Persistência via MySQL 

**Requisitos**
- JDK 11 ou superior
- MySQL 
- Gradle 

**Estrutura do projeto (resumo)**
- `src/main/java/br/com/dio/persistence` — config, entidades, DAOs e migrações
- `src/main/java/br/com/dio/service` — serviços e regras de negócio
- `src/main/java/br/com/dio/ui` — menus de console (`MainMenu`, `BoardMenu`)
- `src/main/resources/db/changelog` — arquivo `db.changelog-master.yml` e scripts SQL de migração

**Adicionar uma nova migração**
1. Coloque o script SQL em `src/main/resources/db/changelog/migrations`.
2. Registre o arquivo no `db.changelog-master.yml` ou adicione um changelog que inclua o novo arquivo.
3. Ao executar a aplicação a migração será aplicada automaticamente.

**Dependências principais**
- `org.liquibase:liquibase-core`
- `mysql:mysql-connector-java`
- `org.projectlombok:lombok`
