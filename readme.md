To use:

just set these env var:

```
VC_API_TOKEN : api token that vividcortex gives you
VC_HOSTNAME (optional): host name to use, to override using docker/k8s given hostname
VC_DRV_MANUAL_HOST_URI (optional): comma-separated list of database URLs to monitor. You can still add hosts using VividCortex's web app. example: <schema>://[<user>[:<password>]@]<host>:<port>[/<db>][?key1=value1&...]
```

example

```bash
docker run -e VC_API_TOKEN={token} canopytax/vividcortex

```


or use a k8s deployment:
```
kubectl run vividcortex --env VC_API_TOKEN={token_here} --image=canopytax/vividcortex --requests=cpu=200m
```
