### Q.5. Setup mickrok8s with one node and deploy nginx server on it.

## Install Microk8s
'''
sudo snap install microk8s --classic 
'''

## Enable Add-ons

'''
sudo microk8s enable dns ingress
'''

## Deploy Nginx server
'''
sudo microk8s kubectl apply -f nginx-deployment.yaml
'''

## Expose Nginx server
'''
sudo microk8s kubectl apply -f nginx-service.yaml
'''

## Get the NodePort
'''
sudo microk8s kubectl get services
'''
## To access the Nginx server

[link text](http://localhost:NODE_PORT)

**Replace the NODE_PORT with the Port number got from the last command**