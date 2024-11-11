![preview](./images/obs1.png)
* premetheus scrape these metrics and store them in TSDB.time stamp of metrics.
* prometheus has a `http sever` using this to get the data from TSDB we can write the `promql` query.
* install the eks and configure the all prommetheus, alert manager node exporter,grafana, and prometheus apiserver.
* `node exporters` runs as a `daemonsets`. it has based on nodes, number of pods.
![preview](./images/obs2.png)
* `kube-state metric` is talk to` k8s api server`. it is only one pod.
![preview](./images/obs3.png)
* we cannot access it from browser because it has clusterip service.
![preview](./images/obs4.png)
![preview](./images/obs5.png)
* goto one of the node and connect the session.
![preview](./images/obs6.png)
![preview](./images/obs7.png)
![preview](./images/obs8.png)
* node exporter will collect the metrics periodically.
![preview](./images/obs9.png)
* prometheus will get the metrics from node exporters.
  * in node exporter there will be a endpoint called `/metrics` on that node exporter will retirn the output.
* if we want to get the metrics from kube state metric server.
![preview](./images/obs10.png)
![preview](./images/obs11.png)
![preview](./images/obs12.png)
![preview](./images/obs13.png)
![preview](./images/obs14.png)
* create a crash pod to check it in prometheus. for that we use busy box.
![preview](./images/obs15.png)
![preview](./images/obs16.png)
* as soon as you created the pod `kube api server` receives the information.
![preview](./images/obs17.png)
![preview](./images/obs18.png)
## grafana
----------------------------------------------------------------------------------------------------
* grafana provide better dashboards. grafana supports multiple datasources.
* it is independent of prometheus.
* it is a visualization platform.not a monitoring tool.
* in grafana u can set authentication and authorization.
  * integrated with IAM or SSO.
![preview](./images/obs19.png)
![preview](./images/obs20.png)
![preview](./images/obs21.png)
* default dashboards in grafana.
![preview](./images/obs22.png)
![preview](./images/obs23.png)
![preview](./images/obs24.png)
![preview](./images/obs25.png)
![preview](./images/obs26.png)
* save the dashboards.
* to add any other dashboards to grfana.
![preview](./images/obs27.png)

## custom metrics
* prometheus will not look all the servicea and all the pods.
* the no of calls increased cpu memory utilization go high.
## service monitor
* service monitor will tell prometheus services to look for?