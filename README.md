# devops-server
1.- Take a simple nodejs server of your choosing, make it installable on kubernetes, then write documentation for a user (in this case, me) to install that server on their own kubernetes.

Assume kubectl installed

$ kubectl create deployment --image viclisa/node-hello-app node-app

$ kubectl expose deployment node-app --type=NodePort --port 3000

At this time we are ready to see the sever in the node IP and port interal

$kubectl get nodes -o wide
IP = internal-ip of node node-app

$minikube kubectl -- get svc
PORT = the second port in the port(S) list in the node-app of type NodePort. The one wich is not 3000

Open a browser and navigate to IP:PORT
