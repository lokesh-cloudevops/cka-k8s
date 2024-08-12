Deployments:
A Deployment provides declarative updates for Pods and ReplicaSets.

Updating image:

kubectl set image deployment/nginx-deployment nginx=nginx:1.16.1

kubectl edit deployment/nginx-deployment

kubectl rollout status deployment/nginx-deployment

kubectl rollout history deployment/nginx-deployment

kubectl rollout pause deployment/nginx-deployment  (After pausing we can edit deploy and we won't get any new rollouts)

kubectl rollout resume deployment/nginx-deployment

kubectl rollout history deployment/nginx-deployment --revision=2 (To see details of each version separately)

kubectl rollout undo deployment/nginx-deployment (Rolling back to prev version)
(or)
kubectl rollout undo deployment/nginx-deployment --to-revision=2 (by specific version)

kubectl scale deployment/nginx-deployment --replicas=10 (scaling deployment)

kubectl set resources deployment/nginx-deployment -c=nginx --limits=cpu=200m,memory=512Mi  (update resources)

kubectl get rs -w (watch the process)

kubectl describe deployments

