## cluster installation
---------------------------------------------------------------------------------------
* [Refer Here](https://github.com/jaya4606/observability-zero-to-hero/tree/main/day-2) for the installations.
![preview](./images/obs1.png)
* install helm.
![preview](./images/obs2.png)
* create a namespace observability.
![preview](./images/obs3.png)
* alert amanger is the custom part.
* do the port forwarding for prometheus and graphana.
![preview](./images/obs4.png)
![preview](./images/obs5.png)
* do port forwarding for premetheus and graphana not use any ingress here.
![preview](./images/obs6.png)
![preview](./images/obs7.png)
![preview](./images/obs8.png)
* alert manager
![preview](./images/obs9.png)
* add datasource as prometheus for graphana.
![preview](./images/obs10.png)
* exporters for prometheus.
  * node exporters.(`infrastructure level metrics`).
    * pull the information from each node.cpu,memory,disk related metrics.
    * it will read the system files of the nodes or virtual machine.
  * kube state metrics exporter(`k8s level metrics`).
    * it will get all information from k8s api server.
    * all pod, events, entire k8s relatd  informations.
    * default installation.
* these two are primary things in prometheus.
* To get the application level metrics,like to get information of http requests, user level signups,how many times a user perform a specific activity on that application.
* to get those deatils the developers of that application should write `metrics server` 
```
/logout - page
/login  - page
/metrics - endpoint
```
* prometheus using the `service discovery` mechanism to scrape the /metrics endpoint of u r application.
![preview](./images/obs11.png)
* prometheus is also CNCF project(second).