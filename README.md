Metrics Exposed by Spring Boot Actuator
When you enable the actuator endpoints and add the micrometer-registry-prometheus dependency, Spring Boot will automatically expose the following metrics in the /actuator/prometheus endpoint:

JVM metrics: memory usage, garbage collection, threads, classes

CPU metrics: system and process CPU usage

File descriptor metrics: open file descriptors

Tomcat metrics: active sessions, active threads, request processing times

Log4j2 metrics: log levels

Logback metrics: log levels (only available if using Logback)

Custom Application Metrics

In addition to the default metrics, you can also define and expose custom application metrics using Micrometer. For example, you can track:

Request counts and latencies for specific endpoints

Cache hits and misses

Database connection pool usage

Specific business metrics relevant to your application

To add custom metrics, you can use Micrometer's Counter, Timer, Gauge, and other metric types.


Once you have the actuator endpoints enabled and the Micrometer Prometheus registry added, you can view the exposed metrics in Prometheus. The metrics will be available at the /actuator/prometheus endpoint of your Spring Boot application.

Prometheus will periodically scrape the metrics from this endpoint and store them in its time-series database. You can then use PromQL (Prometheus Query Language) to query and analyze the metrics.

Grafana allows you to create dashboards that display the metrics collected by Prometheus. You can create graphs, charts, and tables to visualize the data and gain insights into your application's performance and health.
