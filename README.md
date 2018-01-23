# monitoring

## Update alerting rules 
- Run `promtool update rules batch_job.rules` as mentioned here - https://github.com/prometheus/prometheus/issues/2913

## Steps to run
### Bring up the system 
- `docker-compose up`
### Create fat jar 
- `sbt clean assembly` 
### Run spark batch job
- `spark-submit --class=monitoring.batch.job.CountingLocalApp target/scala-2.11/monitoring-assembly-0.0.1.jar sample-data/inputFile.txt sample-data/outputDir`

## URLs 
- Prometheus - http://localhost:9090/graph & http://localhost:9090/metrics
- Push Gateway -  http://localhost:9091/
- Alert Manager -  http://localhost:9093/

## Backlog
- [X] Create sample spark job
- [ ] Schedule spark job using Azkaban
- [X] Post metrics from spark job
- [ ] Create Grafana dashboards to visualize metrics
- [X] Alert on slack channel