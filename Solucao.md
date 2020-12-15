# Trabalho Individual 2020-1

**Aluno**: Eduardo Lima Ribeiro

**Matrícula**: 160049458

### Conteinização

Foi usado o docker e docker-compose para a contenerização do projeto, sendo criados os conteiners 'api' e 'client' para o backend e frontend, respectivamente.

### Integração contínua

Foi usado o Travis CI para a integração contínua do projeto. Ele roda automaticamente a cada build repassada pela master do repositório.

### Como rodar

```
docker-compose up -d --build
```
### Testes front

```
docker-compose run client yarn run test:unit
```

### Testes back

```
docker-compose run api bundle exec rails test
```