# About Udagram

Udagram is a simple cloud application developed alongside the Udacity Cloud Engineering Nanodegree. It allows users to register and log into a web client, post photos to the feed, and process photos using an image filtering microservice.

# Create a Kubernetes cluster on AWS
For that you can use various tools, including [Kubeone](https://github.com/kubermatic/kubeone) and their [AWS quick start guide](https://github.com/kubermatic/kubeone/blob/master/docs/quickstart-aws.md).

# Run the app
Once your Kubernetes cluster is ready you will need to use [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl).

Navigate to `udacity-c3-deployment/docker/k8s`

Apply the secrets:

`kubectl apply -f aws-secret.yaml`

`kubectl apply -f env-secret.yaml`

Appy the ConfigMap:

`kubectl apply -f env-configmap.yaml`


Apply rest of yaml files in the directory:

`kubectl apply -f .`

Open `localhost:8100` to see the app running