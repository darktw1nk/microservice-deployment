# Deployment configurations

Потыкать результат можно тут:http://35.228.236.102/

Так же есть:
1. kibana(логи): http://35.228.107.141:5601
2. alertmanager: http://35.228.64.145:9093
3. grafana: http://35.228.106.158
4. prometheus: http://35.228.197.205:9090
5. jaeger: http://35.228.65.181:16686/

В Grafana логин: admin, пароль: Mahindra  
Jaeger может умереть, поэтому чуть позже будет несколько скриншотов по нему  
  
Может умереть, потому что у бесплатного аккаунта Google Cloud стоят квоты, и им очень не нравится больше определенного количества используемых сервисов и ip адресов и сервис, добавленный последним может умереть, впрочем замечают они это не сразу.

В Grafana есть dashboards по kubernetes кластеру, kafka и можно сделать dashboard по сервисам, но для этого они должны отдавать информацию в prometheus в формате time series

Структура:
![Structure](/images/structure.png)

в итоге получается вот такой кластер:
![Cluster](/images/cluster.png)

Вот пример dashboard в grafana
![Cluster](/images/kafkaDashboard.png)

И несколько jaeger скриншотов
1) Relations между сервисами, кто к кому обращается
![Jaeger1](/images/jaeger1.png)

2) И поближе
![Jaeger2](/images/jaeger2.png)

3) Информация о трейсах, что когда вызывалось и сколько заняло
![Jaeger3](/images/jaeger3.png)

Репозитории:
 1. UI: https://github.com/darktw1nk/microservices-ui
 2. Worker Service: https://github.com/darktw1nk/microservices-worker-service
 3. Statistics Service: https://github.com/darktw1nk/microservices-statistics-service
 4. Project Service: https://github.com/darktw1nk/microservices-project-service
 5. Company Service: https://github.com/darktw1nk/microservices-company-service
 6. User Service: https://github.com/darktw1nk/microservices-user-service
