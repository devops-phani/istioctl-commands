# istioctl-commands

Install istioctl

```
curl -sL https://istio.io/downloadIstioctl | sh -
```

add to path file `~/.bashrc`

```
export PATH=$HOME/.istioctl/bin:$PATH
```

```
source ~/.bashrc
```

```
istioctl proxy-status
```


Ref link
- https://istio.io/latest/docs/ops/diagnostic-tools/istioctl/

Debug the istio proxy

Example

```
istioctl proxy-config log podname.namespacename --level debug
```

Update levels of the specified loggers.

```
istioctl proxy-config log <pod-name[.namespace]> --level http:debug,redis:debug
```

Check the proxy container logs in your pod

```
kubectl -n namespace logs -f podname -c istio-proxy
```
Ref link

- https://medium.com/@chaitanyasolasa1/debugging-in-istio-servicemesh-6a5f150f71be



