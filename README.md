# monitoring

## Steps to run
- `sbt run inputFile outputDir` 
- e.g. `spark-submit --class=monitoring.spark.job.CountingLocalApp  target/scala-2.11/monitoring_2.11-0.0.1.jar  sample-data/inputFile.txt sample-data/outputFile1`

## Backlog
- [X] Create sample spark job
- [ ] Schedule spark job using Azkaban
- [ ] Create Prometheus docker image
- [ ] Post metrics from spark job
- [ ] Create Grafana dashboards to visualize metrics
- [ ] Alert on slack channel