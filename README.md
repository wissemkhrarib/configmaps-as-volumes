# ConfigMaps as volumes

## Create the ConfigMap
First, create a ConfigMap using the redis-conf file using this command
**kubectl create configmap redis-conf --from-file=redis-conf**

## Create the pod and mount the ConfigMap as a volume
To create the pod and mount the ConfigMap as a volume to the pod, apply the redis-pod.yaml to kubernetes using this command
**kubectl create -f redis-pod.yaml**

The mount is done by creating a volume of type ConfigMap and mounting it to the redis container