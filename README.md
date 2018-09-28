Wordpress Deployment on k8s

Create a Secret for MySQL Password
  kubectl create secret generic mysql-pass --from-literal=password=YOUR_PASSWORD

Deploy Volumes
  kubectl apply volumes/

Deploy MySQL
  kubectl apply -f mysql-manifests/

Deploy WordPress
  kubectl apply -f wordpress-manifests/
