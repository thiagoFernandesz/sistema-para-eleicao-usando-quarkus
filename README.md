# Gerenciamento de Eleições

Este projeto utiliza o Quarkus, o Framework Java Supersônico Subatômico.

Se você deseja saber mais sobre o Quarkus, por favor visite seu website: [Quarkus](https://quarkus.io/).

## Executando a aplicação em modo de desenvolvimento

Você pode executar sua aplicação em modo de desenvolvimento, que permite codificação ao vivo, utilizando:

```shell script
./mvnw compile quarkus:dev
```
> **_NOTA:_**  O Quarkus agora vem com uma Interface de Desenvolvimento (Dev UI), que está disponível apenas no modo de desenvolvimento em http://localhost:8080/q/dev/.

## Empacotando e executando a aplicação

A aplicação pode ser empacotada utilizando:

```shell script
./mvnw package
```
Isso produz o arquivo `quarkus-run.jar` no diretório `target/quarkus-app/.`
Atenção que não é um über-jar já que as dependências são copiadas para o diretório target/quarkus-app/lib/.

A aplicação agora pode ser executada utilizando `java -jar target/quarkus-app/quarkus-run.jar.`

Se você deseja construir um über-jar, execute o seguinte comando:

```shell script
./mvnw package -Dquarkus.package.type=uber-jar
```

A aplicação, empacotada como um über-jar, agora pode ser executada utilizando `java -jar target/*-runner.jar.`

## Criando um executável nativo

Você pode criar um executável nativo utilizando:

```shell script
./mvnw package -Pnative
```

Ou, se você não tiver o GraalVM instalado, você pode executar a construção do executável nativo em um contêiner utilizando:

```shell script
./mvnw package -Pnative -Dquarkus.native.container-build=true
```

Você pode então executar seu executável nativo com: `./target/election-management-1.0.0-SNAPSHOT-runner`

Se você deseja saber mais sobre a construção de executáveis nativos, por favor consulte [Maven Tooling.](https://quarkus.io/guides/maven-tooling.).

## Guias Relacionados
Logging GELF ([guia](https://quarkus.io/guides/centralized-log-management)): Registrar usando o Formato de Log Estendido do Graylog e centralizar seus logs no ELK ou EFK

SmallRye Health ([guia](https://quarkus.io/guides/microprofile-health)): Monitorar a saúde do serviço

SmallRye Context Propagation ([guia](https://quarkus.io/guides/context-propagation)): Propagar contextos entre threads gerenciadas em aplicações reativas

RESTEasy Reactive ([guia](https://quarkus.io/guides/resteasy-reactive)): Uma implementação JAX-RS utilizando processamento em tempo de construção e Vert.x. Esta extensão não é compatível com a extensão quarkus-resteasy, ou qualquer uma das extensões que dependem dela.

OpenTelemetry ([guia](https://quarkus.io/guides/opentelemetry)): Use o OpenTelemetry para rastrear serviços.