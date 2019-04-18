# LoggingAndMonitoring
A stack used as example of Docker Logging Driver and Fluentd.


# flow
A dockerize [Spring Boot Application](https://spring.io/guides/gs/spring-boot-docker/) will be running and configured to send console output event to [Fluentd](https://www.fluentd.org/).

The event stream will be forward to [Elasticsearch](https://www.elastic.co/products/elasticsearch) for index this data.

Lastly [Kibana](https://www.elastic.co/products/kibana) will show centralized logging.


# hands-on
First, build dockerized application with [Gradle](https://gradle.org/):

```bash
gradle --project-dir=./webApplication build
```


After that, start all services - except dockerized application:

```bash
docker-compose up -d --build fluentd kibana
```


Finally, just run dockerized application:

```bash
docker-compose up -d app
```
