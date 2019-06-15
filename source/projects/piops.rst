Pi Ops
============

Here lies the documentation for the PI setup I currently have.

Currently I own 3 raspberry pis.

1. Aurelies - Contains sense hat module
#. Athena - No extensions
#. Odin - Contains voice hat module

A custom raspbian image is used to flash the SD cards. 
The image has some pre configured settings and also has docker installed. 
This makes setting up a new PI relatively easy.

Throughout the documentation I will refer to the pis by their name.

.. note:: TODO: Add todo's here.

Technologies
-----------------------------

Kubernetes
~~~~~~~~~~

Kubernetes is used to orchestrate the containers. 
Kubernetes makes it easy to create and deploy services. 
Helm charts will probably used to manage the different deployments.

+--------------+----------+
| Master Nodes | Odin     |
+--------------+----------+
| Slave Nodes  | Athena,  |
|              | Aurelius |
+--------------+----------+

Docker
~~~~~~~~~~

Containers are great for running applications. 
They provide a nice isolated environment to run your apps in.
A local docker registry will contain all the images that kubernetes can pull and use.

Prometheus
~~~~~~~~~~

Prometheus will be used for monitoring and alerts.
Athena runs a prometheus client that broadcasts sense hat readings.
The prometheus server will parse information from various clients and store them.
Grafana is used to present the data for monitoring.

Prometheus also comes with an alert manager. 
This will be hooked to a slack bot and show alerts when failure occurs or performance is unsual.

Grafana
~~~~~~~~~~






