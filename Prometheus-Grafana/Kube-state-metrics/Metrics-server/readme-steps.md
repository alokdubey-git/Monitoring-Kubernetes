Prometheus, kube-state-metrics, Metrics Server, Grafana Example
Run kubectl create namespace monitoring to create a monitoring namespace.

Run kubectl create -f ./ -R to get kube-state-metrics, Grafana, and Prometheus resources in place.

Check NODEIP using:

kubectl get nodes --selector=kubernetes.io/role!=master -o jsonpath={.items[*].status.addresses[?\(@.type==\"InternalIP\"\)].address}

Visit http://[NODEIP]:30000 to view Prometheus.

Click on Graph. Select a metric from the drop-down (next to the Execute button) and then click Execute. You can switch between the Graph view and Console view.

NOTE: The Metrics Server YAML can be modified to enable it to run in more simple Kubernetes scenarios like Docker Desktop.

Removing Resources
To remove all of the monitoring resources run kubectl delete -f ./ -R.

Additional Details
Get more details on Prometheus at https://prometheus.io/docs/prometheus/latest/getting_started and https://devopscube.com/setup-prometheus-monitoring-on-kubernetes.

A list of Pod Metrics provided by kube-state-metrics can be found at https://github.com/kubernetes/kube-state-metrics/blob/master/docs/pod-metrics.md.
