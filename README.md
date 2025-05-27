# java-spring-camel-otel-jaeger-postgres-mysql_consumoapis
Exemplo de aplicação criada com Java + Spring + Apache Camel e utilizando Distributed Tracing com Jaeger + OpenTelemetry (configurando porta do Collector) e consumindo APIs REST (uma destas depende de bases PostgreSQL + MySQL). Inclui o uso de Docker Compose para a subida de ambiente que faz uso do projeto Jaeger e do OpenTelemetry Collector.

APIs REST utilizadas por este projeto:
- [**Contagem de acessos (.NET 9 + ASP.NET Core)**](https://github.com/renatogroffe/aspnetcore9-otel-jaeger-postgres-mysql_apicontagem)
- [**Saudações (Node.js)**](https://github.com/renatogroffe/nodejs-otel-jaeger_apisaudacoes)

Agents Java do OpenTelemetry: **https://github.com/open-telemetry/opentelemetry-java-instrumentation/releases**

Variáveis de ambiente a serem configuradas para uso de tracing distribuído com Jaeger:

Essas variáveis podem ser configuradas no Eclipse IDE através do menu **Run > Run Configurations... > Environment**:

![Variáveis de ambiente no Eclipse](img/eclipse-env-var-jaeger.png)

Já o Agent Java do OpenTelemetry foi configurado em **Run > Run Configurations... > Arguments > VM arguments**:

![Configurando uso do Agent Java do OpenTelemetry no Eclipse](img/eclipse-env-var-jaeger.png)

Traces gerados durante testes no dashboard do Jaeger:

![Traces gerados no Jaeger](img/jaeger-01.png)

Exemplo de trace demonstrando uma interação entre as 3 aplicações aqui mencionadas:

![Trace em detalhes no Jaeger](img/jaeger-02.png)