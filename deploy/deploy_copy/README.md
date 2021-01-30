Kubernetes manifests to be used to deploy the whole application:

To deploy mongodb in your local cluster or GKE step:

Describtion:

This is k8s manifest to deploy python ticketing application with mongodb database.

To deploy mongodb database  with dynamic persistent volume and service.  

$ kubectl apply -f mongo-db/

Note: The python application will connect automatically to database using dns: mongo-db-0.database

To deploy the Python app:

It's deployment manifest with 1 replicas and service type "Loadblancer" with external IP address.
Steps:
    1- build docker image and push it to gcr.
    2- specify the image in python-app/ticketing-app-deployment.yaml

$ kubectl apply -f python-app/

