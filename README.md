## Proof of concept for monitoring neo4j
___

A preconfigured  neo4j enterprise edition single cluster installation which 
exposes metrics through a Prometheus endpoint. Metrics as shipped to 
ElasticSearch for indexing and visualization plus an open source GUI for
monitoring neo4j cluster with basic dashboards already setup.

Run `docker compose up` to spin up:

* ELK stack based on 7.3.1
* neo4j 3.5.13 enterprise edition
* metricbeat 7.5.0
* Halin Neo4j Monitoring GUI


### Kibana
Available at `http://localhost:5601/`. 
Login credentials
* username: `elastic`
* password: `changeme`

Remember to create an index after during first login!

### Neo4j Prometheus enpoint
Available at `http://localhost:2004/metrics`

### Halin Neo4j Monitoring GUI
Available at `http://localhost:3000`
Login credentials to connect to neo4j
* username: `neo4j`
* password: `neo4j`

❗ WARNING: Be patient: During intital execution, it will take some time before the
all dependencies are pull down and the server is available!