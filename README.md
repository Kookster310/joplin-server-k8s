# joplin-server-k8s
*run joplin-server in kubernetes on arm64*

Confirmed working in k3s cluster hosted on 4* LePotatos (arm64). 

### Steps
- Create namespace
```kubectl create ns joplin-server-ns```
- Update config maps with your configurations (password, stmp, etc.)
`joplin-server-k8s/db.configmap.yaml`
`joplin-server-k8s/app.configmap.yaml`
- Deploy
```kubectl apply -ff joplin-server-k8s/```

need to do: add ingress
