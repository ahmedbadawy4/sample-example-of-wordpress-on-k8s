# This projecr describe how to install wordpress on kubernetes 

# Wordpress Deployment on k8s:

Create a Secret for MySQL Password:
  
kubectl create secret generic mysql-pass --from-literal=password=YOUR_PASSWORD

Deploy Volumes:
  
kubectl apply -f volumes/

Deploy MySQL:
  
kubectl apply -f mysql-manifests/

Deploy WordPress:
  
kubectl apply -f wordpress-manifests/

Run the following command to get the IP Address for the WordPress Service:
  
minikube service wordpress --url
