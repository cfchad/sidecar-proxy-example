# sidecar-proxy-example
Example application for article at https://medium.com/@lukas.eichler/securing-pods-with-sidecar-proxies-d84f8d34be3e about Kubernetes Sidecar proxies

## Run locally with Docker

```shell
docker build nginx-proxy -t cfchad/nginx-proxy
docker run -v $PATH_TO_PROJECT/sidecar-proxy-example/htpasswd:/etc/nginx/passwd/htpasswd -it -p 8085:80 cfchad/nginx-proxy
```

## Generate Username and Password with htpasswd

```shell
### Print to shell
$ htpasswd -nb admin admin
admin:$apr1$u7/Ys0KC$Cazmt69orKLRlgfLo53K00

### Create file htpasswd
$ htpasswd -b -c htpasswd admin admin
Adding password for user admin
```
