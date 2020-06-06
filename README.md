# sample-django-hpa

This repository focuses on deploying workload on Kubernetes with Horizontal Pod Auto Scaling resource.

#### Create a simple Kubernetes manifest to expose a django application with database server with the following config

There should be 10 replicas running.
The deployment should autoScale at average 50% cpu and 60% memory.
Use a custom docker image hosted on private docker registry called docker.io/tathagatk22/django-app:1.
Expose the app on port 80 via Load Balancer.

### Deployment

```
$ git clone https://github.com/tathagatk22/sample-django-hpa.git
$ kubectl create secret docker-registry regcred --docker-server=docker.io --docker-username=<username> --docker-password="<password>" 
$ kubectl apply -f .
```