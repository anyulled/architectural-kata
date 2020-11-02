#ADR16. Services testability

## STATUS
Accepted

## CONTEXT


## DESCRIPTION
We want metrics and alerts to know how well our services work, and to know when there's a problem. 

## DECISION
Accepted.

## DETAILS
We want to build modern, fast, secure, responsive web apps, etc. 
Rather than build, we want to purchase.

### Constraints

We want tooling that works well with our devops pipeline and with our deployment clouds.

### Positions

We are researching for using a solution based on:

* ELK
* Grafana
* InfluxDB
* Nagios
* Prometheus
* DataDog
* New Relic
* Dynatrace
* Telegraf
* Splunk

### Argument

ELK has the best open-source build-over-buy popularity.

The most famous one is Prometheus + Graphana.

Zabbix has the best recommendations, and also offers the most complete capabilities.

The oldest, shortest, open, viable tool is Nagios. New Relic is the newest, most complete, paid, feasible tool featured.

### Consequences

Free tier vs Pais tier

## Notes

A pretty good open source stack is:

* Prometheus for metrics and alerting based on metrics
* Grafana to display metrics
* Elasticsearch/Logstash/Kibana (ELK) for logs and structured events
