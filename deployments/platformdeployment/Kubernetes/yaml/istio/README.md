# Istio

## namespace

name: yelb

## deployments

* yelb-ui
  * image: mreferre/yelb-ui:0.7
  * port: 80

* redis-server
  * image: redis:4.0.2
  * port: 6379

* yelb-db
  * image: mreferre/yelb-db:0.5
  * port: 5432

* yelb-appserver
  * image: mreferre/yelb-appserver:0.5
  * port: 4567

## services

* yelb-db
  * port: 6379
  * type: ClusterIP

* redis-server
  * port: 6379
  * type: ClusterIP

* yelb-appserver
  * port: 4567
  * type: ClusterIP

* yelb-ui
  * port: 80
  * type: ClusterIP