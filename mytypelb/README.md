# MyTypeLB

The following is a simple PoC of using type:LoadBalancer with
Container Ingress Services 2.0.0

The process is to assign a service that includes "loadBalancerIP"

This script will identify these resources and create a BIG-IP
VirtaulServer with the IP address specified.

## Installing the script

```
pip install -r requirements.txt
```

## Running the Script

This script assumes that you have a kubeconfig file with
appropriate privileges.

```
./mytypelb.py
```

## Known issues

-Only uses a single port from the service (workaround: create multiple services with same loadBalancerIP
-hardcodes "default" namespace and name of configmap
