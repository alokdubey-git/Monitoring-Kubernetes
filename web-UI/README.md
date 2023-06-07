Kubernetes Dashboard (Web UI)
Dashboard is a web-based Kubernetes user interface. We can use Dashboard to get an overview of applications running on our cluster, as well as for creating or modifying individual Kubernetes resources.Dashboard also provides information on the state of Kubernetes resources in your cluster and on any errors that may have occurred.

Configuration Steps:
Deploy the Kubernetes Dashboard UI:

kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.0.0/aio/deploy/recommended.yaml

Run kubectl apply -f dashboard-adminuser.yml to create a new user.

Run kubectl proxy to access the Dashboard UI.

Visit http://localhost:8001/api/v1/namespaces/kubernetes-dashboard/services/https:kubernetes-dashboard:/proxy/

Get a token by running the following command and copy the token into your clipboard.

kubectl -n kubernetes-dashboard get secret $(kubectl -n kubernetes-dashboard get sa/admin-user -o jsonpath="{.secrets[0].name}") -o go-template="{{.data.token | base64decode}}"

Paste the token into the login screen and you can then sign in to the dashboard.

To create a resource from dashboard:
Click on + and then upload the newDeploy.yml manifest file. This will create a new deployment resource for us.
Useful Reference links:
Deploying Dashboard UI
Creating Sample User -Official Dashboard Github Repository
