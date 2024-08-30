Config map and secrets:


What is a config map in Kubernetes?
When your manifest grows it becomes difficult to manage multiple env vars
You can take this out of the manifest and store as a config map object in the key-value pair
Then you can inject that config map into the pod
You can reuse the same config map into multiple pods

Imperative method:
#Command
Kubectl create cm app-cm --from-literal=firstname=lokesh \ --from-literal=lastname=kumar    

#from file
kubectl create cm app-cm --from-file=app.config



Secrets:

Follow the doc: https://kubernetes.io/docs/tasks/inject-data-application/distribute-credentials-secure/#define-container-environment-variables-using-secret-data
