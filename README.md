# meetupdocker
Docker meetup 


Django Deployement Steps:

1. Activate the dev environment: source bin/activate
2. Create the Docker file
3. ibmcloud cr build -t registry.ng.bluemix.net/vthink/djangoapp1:2 .   (Build the docker image for the folder)
4. Run the django image pushed on to IBM Cloud (kubectl run djangosvc1 --image=registry.ng.bluemix.net/vthink/djangoapp:1)
5. At this point the django deployment is created, now expose it
6. kubectl expose deployment/django --type=NodePort --name=djangoappsvc --port=8000
