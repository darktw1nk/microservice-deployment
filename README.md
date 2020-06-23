# Deployment configurations

just a very basic "Game Dev Tycoon"-like web application
It was made for educational purposes and to look into depth of kubernetes, kafka, jaeger, GraalVM and others interesting things

you can try result here:http://35.228.98.121/

23.06.2020: be notified! it will die in a few days, as google cloud test period is limited
And all systems below already died to extend an existence of main application (statistics also died)

Also you can check:
1. kibana(логи): http://35.228.107.141:5601
2. alertmanager: http://35.228.64.145:9093
3. grafana: http://35.228.106.158
4. prometheus: http://35.228.197.205:9090
5. jaeger: http://35.228.65.181:16686/

Grafana login: admin, password: Mahindra  

As Jaeger is a least important component i will disable it soon, cloud resources is limited and by disabling jareger and other systems i may extend lifetime of all other components. Due to this i will attach some screenshots from it at the bottom of this page  
  
Grafana contains dashboards for kubernetes cluster, kafka and we may create dashboard for each service, but we need to implement information retrieval in time series format for prometheus

Structure:
![Structure](/images/structure.png)

Cluster:
![Cluster](/images/cluster.png)

Grafana dashboard example
![Cluster](/images/kafkaDashboard.png)

Few Jarger screenshots
1) Relations between services
![Jaeger1](/images/jaeger1.png)

2) Closer look
![Jaeger2](/images/jaeger2.png)

3) Trace information, which methods has been called and how much time it took
![Jaeger3](/images/jaeger3.png)

Repositories:
 1. UI: https://github.com/darktw1nk/microservices-ui
 2. Worker Service: https://github.com/darktw1nk/microservices-worker-service
 3. Statistics Service: https://github.com/darktw1nk/microservices-statistics-service
 4. Project Service: https://github.com/darktw1nk/microservices-project-service
 5. Company Service: https://github.com/darktw1nk/microservices-company-service
 6. User Service: https://github.com/darktw1nk/microservices-user-service
