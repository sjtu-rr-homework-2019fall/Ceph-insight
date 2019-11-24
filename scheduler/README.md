### Random Kubernetes scheduler On Microk8s

This is a custom kubernetes scheduler that can be used for tutorials.
It's not intended for production usage.

The scheduler watches pods and binds them to random nodes, then emits "Scheduled" events.

Just run `sudo docker build -t macoredroid/scheduler:v0.2 .` to build the image.

Then you can run `sudo microk8s.kubectl apply -f deployment.yaml` to deploy the scheduler on microk8s.

Remember that if you add serviceAcount to spec, you will fail to run that scheduler on microk8s.

I should give credit to [this article]( https://banzaicloud.com/blog/k8s-custom-scheduler/ )

