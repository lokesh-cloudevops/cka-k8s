

![alt text](image.png)

![alt text](image-1.png)


kubectl autoscale deploy php-apache --cpu-percent=50 --min=1 --max=5

Increase the load:
kubectl run -i --tty load-generator --rm --image=busybox:1.28 --restart=Never -- /bin/sh -c "while sleep 0.01; do wget -q -O- http://php-apache; done"

kubectl get hpa php-apache --watch