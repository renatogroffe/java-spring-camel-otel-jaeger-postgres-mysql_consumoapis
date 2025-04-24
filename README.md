# java-spring-camel-otel-jaeger-postgres-mysql_consumoapis
Exemplo de aplicação criada com Java + Spring + Apache Camel e utilizando Distributed Tracing com Jaeger + OpenTelemetry (configurando porta do Collector) e consumindo APIs REST (uma destas depende de bases PostgreSQL + MySQL). Inclui o uso de Docker Compose para a subida de ambiente que faz uso do projeto Jaeger e do OpenTelemetry Collector.

APIs REST utilizadas por este projeto:
- [**Contagem de acessos (.NET 9 + ASP.NET Core)**](https://github.com/renatogroffe/aspnetcore9-otel-jaeger-postgres-mysql_apicontagem)
- [**Saudações (Node.js)**](https://github.com/renatogroffe/nodejs-otel-jaeger_apisaudacoes)

Agents Java do OpenTelemetry: **https://github.com/open-telemetry/opentelemetry-java-instrumentation/releases**