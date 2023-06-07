Monitoring-Kubernetes-Cluster

This repository holds files and docs for the coursera project, Monitoring Kubernetes Cluster using Kubernetes Dashboard, Prometheus and Grafana.

Project Structure

The whole project is divided into five tasks:

Introduction and Cluster Creation.
Creating Deployment
Deploying Kubernetes Dashboard (Web-UI)
Using Prometheus
Using Grafana Dashboards
Cluster Creation Steps
Step#1: First we will create a cluster using:

kind create cluster

Step#2: Check cluster

kind get clusters

Step#3: Get cluster info

kubectl cluster-info

Step#5: Check Nodes

 kubectl get nodes

Step#6: Check All

kubectl get all -A
