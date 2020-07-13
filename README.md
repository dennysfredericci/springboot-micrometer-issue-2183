# Micrometer Test - Issue 2183

That is a simple spring boot app to test the issue Micrometer issue [#2183](https://github.com/micrometer-metrics/micrometer/pull/2183)

The log4j2 is already configured to use async logging.

###How to test

1 - Change the micrometer-core version on pom.xml to the desired version.

2 - Run the application and call the endpoint http://localhost:8080/home this will execute log.info statement

3 - Check the metrics on actuator endpoint http://localhost:8081/actuator/metrics/log4j2.events?tags=level:info

4 - Repeat the steps 2 and 3 to compare the number of log.info executions and the counter from micrometer.
