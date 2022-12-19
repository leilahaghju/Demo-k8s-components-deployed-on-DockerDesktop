# Demo-k8s-components-deployed-on-DockerDesktop

Here i deploy some k8s components on Docket Desktop. There is one MONGODB and one MONGOEXPRESS which you can see in your browser by http. for this we need one mongo-db deployment+service(internatl) and one mongo-express deployment+service(Internal) and one ingress-controller(nginx) and one ingress.


#ATTENTION
1) For ingress-controller i use this yaml file:
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.5.1/deploy/static/provider/cloud/deploy.yaml

2) all componnets are installed in ingress-nginx namespace and just by running:  "kubectl apply -f "file.yaml""

3) You should insert base64 words in  your secrets.yaml file. to do this you can simply run:   echo -n ""yourtext"|base64
 
4) to check the whole service run this http://kubernetes.docker.internal/ in your browser and you will see something like this:

![image](https://user-images.githubusercontent.com/77623452/208393394-cbe64853-0408-47df-9dbc-5fb10a1130e2.png)

and for testing if every thing is working ok , you can add one new database like below:

![image](https://user-images.githubusercontent.com/77623452/208393787-45e43c0f-d7d0-4869-a15c-d9eb94f23cc2.png)
