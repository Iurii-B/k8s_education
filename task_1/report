USERNAME@PCNAME MINGW64 ~
$ kubectl version --client
Client Version: version.Info{Major:"1", Minor:"22", GitVersion:"v1.22.0", GitCommit:"c2b5237ccd9c0f1d600d3072634ca66cefdf272f", GitTreeState:"clean", BuildDate:"2021-08-04T18:03:20Z", GoVersion:"go1.16.6", Compiler:"gc", Platform:"windows/amd64"}

USERNAME@PCNAME MINGW64 ~
$ kubectl cluster-info
Kubernetes control plane is running at https://192.168.99.100:8443
CoreDNS is running at https://192.168.99.100:8443/api/v1/namespaces/kube-system/services/kube-dns:dns/proxy

To further debug and diagnose cluster problems, use 'kubectl cluster-info dump'.

USERNAME@PCNAME MINGW64 ~
$ kubectl get nodes
NAME       STATUS   ROLES                  AGE   VERSION
minikube   Ready    control-plane,master   18m   v1.22.2


USERNAME@PCNAME MINGW64 ~
$  kubectl get pod -n kubernetes-dashboard
No resources found in kubernetes-dashboard namespace.

USERNAME@PCNAME MINGW64 ~
$ kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.3.1/aio/deploy/recommended.yaml
namespace/kubernetes-dashboard created
serviceaccount/kubernetes-dashboard created
service/kubernetes-dashboard created
secret/kubernetes-dashboard-certs created
secret/kubernetes-dashboard-csrf created
secret/kubernetes-dashboard-key-holder created
configmap/kubernetes-dashboard-settings created
role.rbac.authorization.k8s.io/kubernetes-dashboard created
clusterrole.rbac.authorization.k8s.io/kubernetes-dashboard created
rolebinding.rbac.authorization.k8s.io/kubernetes-dashboard created
clusterrolebinding.rbac.authorization.k8s.io/kubernetes-dashboard created
deployment.apps/kubernetes-dashboard created
service/dashboard-metrics-scraper created
Warning: spec.template.metadata.annotations[seccomp.security.alpha.kubernetes.io/pod]: deprecated since v1.19; use the "seccompProfile" field instead
deployment.apps/dashboard-metrics-scraper created

USERNAME@PCNAME MINGW64 ~
$  kubectl get pod -n kubernetes-dashboard
NAME                                         READY   STATUS              RESTARTS   AGE
dashboard-metrics-scraper-856586f554-w9scc   0/1     ContainerCreating   0          3s
kubernetes-dashboard-67484c44f6-5vgm6        0/1     ContainerCreating   0          3s

USERNAME@PCNAME MINGW64 ~
$ kubectl get deploy
No resources found in default namespace.

USERNAME@PCNAME MINGW64 ~
$ source <(kubectl completion bash)

USERNAME@PCNAME MINGW64 ~
$ kubectl.exe get deploy
No resources found in default namespace.

USERNAME@PCNAME MINGW64 ~
$  kubectl get pod -n kubernetes-dashboard
NAME                                         READY   STATUS    RESTARTS   AGE
dashboard-metrics-scraper-856586f554-w9scc   1/1     Running   0          4m12s
kubernetes-dashboard-67484c44f6-5vgm6        1/1     Running   0          4m12s

USERNAME@PCNAME MINGW64 ~
$  kubectl get ns
NAME                   STATUS   AGE
default                Active   23m
kube-node-lease        Active   23m
kube-public            Active   23m
kube-system            Active   23m
kubernetes-dashboard   Active   4m17s

USERNAME@PCNAME MINGW64 ~
$

USERNAME@PCNAME MINGW64 ~
$

USERNAME@PCNAME MINGW64 ~
$ kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml
serviceaccount/metrics-server created
clusterrole.rbac.authorization.k8s.io/system:aggregated-metrics-reader created
clusterrole.rbac.authorization.k8s.io/system:metrics-server created
rolebinding.rbac.authorization.k8s.io/metrics-server-auth-reader created
clusterrolebinding.rbac.authorization.k8s.io/metrics-server:system:auth-delegator created
clusterrolebinding.rbac.authorization.k8s.io/system:metrics-server created
service/metrics-server created
deployment.apps/metrics-server created
apiservice.apiregistration.k8s.io/v1beta1.metrics.k8s.io created

USERNAME@PCNAME MINGW64 ~
$ kubectl edit -n kube-system deployment metrics-server



USERNAME@PCNAME MINGW64 ~
$ kubectl describe sa -n kube-system default
Name:                default
Namespace:           kube-system
Labels:              <none>
Annotations:         <none>
Image pull secrets:  <none>
Mountable secrets:   default-token-7srp7
Tokens:              default-token-7srp7
Events:              <none>

USERNAME@PCNAME MINGW64 ~
$ ^C

USERNAME@PCNAME MINGW64 ~
$ kubectl get secrets -n kube-system
NAME                                             TYPE                                  DATA   AGE
attachdetach-controller-token-zzlm8              kubernetes.io/service-account-token   3      56m
bootstrap-signer-token-tdxzc                     kubernetes.io/service-account-token   3      56m
bootstrap-token-tuuyor                           bootstrap.kubernetes.io/token         6      56m
certificate-controller-token-6mddm               kubernetes.io/service-account-token   3      56m
clusterrole-aggregation-controller-token-6rrxx   kubernetes.io/service-account-token   3      56m
coredns-token-55hq6                              kubernetes.io/service-account-token   3      56m
cronjob-controller-token-2f67j                   kubernetes.io/service-account-token   3      56m
daemon-set-controller-token-dl4jg                kubernetes.io/service-account-token   3      56m
default-token-7srp7                              kubernetes.io/service-account-token   3      56m
deployment-controller-token-chdbr                kubernetes.io/service-account-token   3      56m
disruption-controller-token-6vddr                kubernetes.io/service-account-token   3      56m
endpoint-controller-token-wpfwj                  kubernetes.io/service-account-token   3      56m
endpointslice-controller-token-n7zp2             kubernetes.io/service-account-token   3      56m
endpointslicemirroring-controller-token-km22f    kubernetes.io/service-account-token   3      56m
ephemeral-volume-controller-token-r56d7          kubernetes.io/service-account-token   3      56m
expand-controller-token-mdbrs                    kubernetes.io/service-account-token   3      56m
generic-garbage-collector-token-m4htw            kubernetes.io/service-account-token   3      56m
horizontal-pod-autoscaler-token-9nh5v            kubernetes.io/service-account-token   3      56m
job-controller-token-t4pvw                       kubernetes.io/service-account-token   3      56m
kube-proxy-token-nl2lp                           kubernetes.io/service-account-token   3      56m
metrics-server-token-vm69t                       kubernetes.io/service-account-token   3      25m
namespace-controller-token-vv9dp                 kubernetes.io/service-account-token   3      56m
node-controller-token-n58xj                      kubernetes.io/service-account-token   3      56m
persistent-volume-binder-token-kf7pf             kubernetes.io/service-account-token   3      56m
pod-garbage-collector-token-24vln                kubernetes.io/service-account-token   3      56m
pv-protection-controller-token-ts5bm             kubernetes.io/service-account-token   3      56m
pvc-protection-controller-token-fhc2q            kubernetes.io/service-account-token   3      56m
replicaset-controller-token-6jmtq                kubernetes.io/service-account-token   3      56m
replication-controller-token-cbr8w               kubernetes.io/service-account-token   3      56m
resourcequota-controller-token-nhvnl             kubernetes.io/service-account-token   3      56m
root-ca-cert-publisher-token-jb7g2               kubernetes.io/service-account-token   3      56m
service-account-controller-token-bp589           kubernetes.io/service-account-token   3      56m
service-controller-token-qhk6l                   kubernetes.io/service-account-token   3      56m
statefulset-controller-token-pvv6z               kubernetes.io/service-account-token   3      56m
storage-provisioner-token-rmwf8                  kubernetes.io/service-account-token   3      56m
token-cleaner-token-t2ll5                        kubernetes.io/service-account-token   3      56m
ttl-after-finished-controller-token-c97qf        kubernetes.io/service-account-token   3      56m
ttl-controller-token-5sb5j                       kubernetes.io/service-account-token   3      56m

USERNAME@PCNAME MINGW64 ~
$ kubectl get secrets -n kube-system default-token-7srp7 -o yaml
apiVersion: v1
data:
  ca.crt: LS0tLS1CRUdJTiBDRVJUSUZJQ0FURS0tLS0tCk1JSURCakNDQWU2Z0F3SUJBZ0lCQVRBTkJna3Foa2lHOXcwQkFRc0ZBREFWTVJNd0VRWURWUVFERXdwdGFXNXAKYTNWaVpVTkJNQjRYRFRJeE1UQXhPREV6TURBME1Wb1hEVE14TVRBeE56RXpNREEwTVZvd0ZURVRNQkVHQTFVRQpBeE1LYldsdWFXdDFZbVZEUVRDQ0FTSXdEUVlKS29aSWh2Y05BUUVCQlFBRGdnRVBBRENDQVFvQ2dnRUJBS1dyCnpyeTRXUElDL2ZnQ1RjM3l3WnZ5RzY4WFYxQzZRM0k0d0V5SW9nT05xWlArMHUrdzJ2Z2JmMnhLZzdnbitTT3EKMGFER2tnUDZBdTIvUFVtbmp5SEVVZElKcmk2UDBwNllvQnV3NXRSNUlZVEo5N29Bd2NNcUFRS3hTemU1WlRSeAplbTV1aXNCc2xvU0VZNjlKamtObkptVGJqSVlKdFcxaXRKMzlidlFXdDRUQVdmNENxbGk1Wit6TlZGQm45ZmxGClk4dGxtcXVzMUF3VnIrTkpHUENjMmVwNEV4M2cxdjY2c0xXUFBObE1mL042SFVIaE96MkYxTVNDMFBOb2VxdDEKRDRtYUgzaFU5bm5XRFdvcTJJL1k2Nkx6TlhjQS9mYldkczUwaTBZdGk0aFNSWmVsMzBJWHQwZ2tXeXJDbWFSRApzb0RHNWY4R2F0SFZRVlpnWURrQ0F3RUFBYU5oTUY4d0RnWURWUjBQQVFIL0JBUURBZ0trTUIwR0ExVWRKUVFXCk1CUUdDQ3NHQVFVRkJ3TUNCZ2dyQmdFRkJRY0RBVEFQQmdOVkhSTUJBZjhFQlRBREFRSC9NQjBHQTFVZERnUVcKQkJTV3BrT2wrWTg1MCszK1lyczZNbUZzNEpxcTJqQU5CZ2txaGtpRzl3MEJBUXNGQUFPQ0FRRUFRNllFWnZTOQp5MlhKcFFTdUNmQStWNFkzSXRBekJSUzRhTHl6bUlhbzl4d2xPQzFXdDlTSnFOcllJU1JSUEFZNHhjbFQ1djJVCi9JQWY3YjlCaURwSlVpWTladjFBSTJ4cjFYbUVzMmxlVFN0Qk5TUjg1eit4STR0c0JCZWlSQzhidEZHMTQ3VUQKZGU1S2xZTSs3ZWJCU05XcVp2ckt1L3k0cGNkZVp6VlVmSm81OVJONDM5c1RUcjd6RlBjZHpySFFIZkxTN1NuNwpqb1duYWtuQXJoZ1p6ME1zanlPdlQyNElyMlNXN0ZwSmtUQmE1MVUvRGpXSEtISmZHU2JPREVjdWpGRm15RE11CjBoZEpITGJBRHY4YWwzNE1QdktFeVM1cDVFYTY3eXVXd0EwWlA2dTJMam53SE9TN3picUZUaklUTHFLNnpsRlkKOXgxcjdvTHhSTTAwckE9PQotLS0tLUVORCBDRVJUSUZJQ0FURS0tLS0tCg==
  namespace: a3ViZS1zeXN0ZW0=
  token: ZXlKaGJHY2lPaUpTVXpJMU5pSXNJbXRwWkNJNkltcEpjWGRET0ZNelJrNVRhR3BFZEVoaWR5MXZNMHAwYkZSdVluSkZRekpZVlhZMmR6TTFMVXg0UTI4aWZRLmV5SnBjM01pT2lKcmRXSmxjbTVsZEdWekwzTmxjblpwWTJWaFkyTnZkVzUwSWl3aWEzVmlaWEp1WlhSbGN5NXBieTl6WlhKMmFXTmxZV05qYjNWdWRDOXVZVzFsYzNCaFkyVWlPaUpyZFdKbExYTjVjM1JsYlNJc0ltdDFZbVZ5Ym1WMFpYTXVhVzh2YzJWeWRtbGpaV0ZqWTI5MWJuUXZjMlZqY21WMExtNWhiV1VpT2lKa1pXWmhkV3gwTFhSdmEyVnVMVGR6Y25BM0lpd2lhM1ZpWlhKdVpYUmxjeTVwYnk5elpYSjJhV05sWVdOamIzVnVkQzl6WlhKMmFXTmxMV0ZqWTI5MWJuUXVibUZ0WlNJNkltUmxabUYxYkhRaUxDSnJkV0psY201bGRHVnpMbWx2TDNObGNuWnBZMlZoWTJOdmRXNTBMM05sY25acFkyVXRZV05qYjNWdWRDNTFhV1FpT2lJMk1HSmhNemhrWlMxak5EUXhMVFJtWVRndE9XWXlPQzFrTlRsbE5EUXlNemszTVdJaUxDSnpkV0lpT2lKemVYTjBaVzA2YzJWeWRtbGpaV0ZqWTI5MWJuUTZhM1ZpWlMxemVYTjBaVzA2WkdWbVlYVnNkQ0o5LkI5akZJQmZoV3RpTUpqUml6MGJWNjdFd1RpT280RzZaalBwODBrWmVqOUJhalpXZzVGQVBOTXBFS1RoRXpUcWhsYmREV0N4YlJBVjJLdGVwMVRIRnI4TFBFNFZGR0VZcFk2aHA0YjFTZURRSGNVU2haVGZCZ3k5WDl4VmtZRE42NjZEeFJMN2ZYUFk2QXkwVzdaVEV6X1Ezc09XN3JRS25uR2xoQi03U2ZQSTdXUng5SWlWYXJSZHp1Q2JsMVJ2amwzODZnNjdaVnI3M3BXTm1lQVJzbFhMUDZBenBxVEF4NXF2WFd6NkFuNV9jejFUYnk1VU02ODlCWGJLTUlmV2p0LVZMT1hhcDhqUWh0ZXpOWGlZWEZkcHZYbUo2VGNZZDVTYlJLZnN6VnBEWHROWTdRTDYwbFhSSkc1T1BSbkEwQjl2LWZPUXhZUTNGa3VmbkpCNmdhUQ==
kind: Secret
metadata:
  annotations:
    kubernetes.io/service-account.name: default
    kubernetes.io/service-account.uid: 60ba38de-c441-4fa8-9f28-d59e4423971b
  creationTimestamp: "2021-10-19T13:01:08Z"
  name: default-token-7srp7
  namespace: kube-system
  resourceVersion: "409"
  uid: 58c67a7c-824e-4894-98fc-bcc65f9f3ce5
type: kubernetes.io/service-account-token



USERNAME@PCNAME MINGW64 ~
$ echo -n "ZXlKaGJHY2lPaUpTVXpJMU5pSXNJbXRwWkNJNkltcEpjWGRET0ZNelJrNVRhR3BFZEVoaWR5MXZNMHAwYkZSdVluSkZRekpZVlhZMmR6TTFMVXg0UTI4aWZRLmV5SnBjM01pT2lKcmRXSmxjbTVsZEdWekwzTmxjblpwWTJWaFkyTnZkVzUwSWl3aWEzVmlaWEp1WlhSbGN5NXBieTl6WlhKMmFXTmxZV05qYjNWdWRDOXVZVzFsYzNCaFkyVWlPaUpyZFdKbExYTjVjM1JsYlNJc0ltdDFZbVZ5Ym1WMFpYTXVhVzh2YzJWeWRtbGpaV0ZqWTI5MWJuUXZjMlZqY21WMExtNWhiV1VpT2lKa1pXWmhkV3gwTFhSdmEyVnVMVGR6Y25BM0lpd2lhM1ZpWlhKdVpYUmxjeTVwYnk5elpYSjJhV05sWVdOamIzVnVkQzl6WlhKMmFXTmxMV0ZqWTI5MWJuUXVibUZ0WlNJNkltUmxabUYxYkhRaUxDSnJkV0psY201bGRHVnpMbWx2TDNObGNuWnBZMlZoWTJOdmRXNTBMM05sY25acFkyVXRZV05qYjNWdWRDNTFhV1FpT2lJMk1HSmhNemhrWlMxak5EUXhMVFJtWVRndE9XWXlPQzFrTlRsbE5EUXlNemszTVdJaUxDSnpkV0lpT2lKemVYTjBaVzA2YzJWeWRtbGpaV0ZqWTI5MWJuUTZhM1ZpWlMxemVYTjBaVzA2WkdWbVlYVnNkQ0o5LkI5akZJQmZoV3RpTUpqUml6MGJWNjdFd1RpT280RzZaalBwODBrWmVqOUJhalpXZzVGQVBOTXBFS1RoRXpUcWhsYmREV0N4YlJBVjJLdGVwMVRIRnI4TFBFNFZGR0VZcFk2aHA0YjFTZURRSGNVU2haVGZCZ3k5WDl4VmtZRE42NjZEeFJMN2ZYUFk2QXkwVzdaVEV6X1Ezc09XN3JRS25uR2xoQi03U2ZQSTdXUng5SWlWYXJSZHp1Q2JsMVJ2amwzODZnNjdaVnI3M3BXTm1lQVJzbFhMUDZBenBxVEF4NXF2WFd6NkFuNV9jejFUYnk1VU02ODlCWGJLTUlmV2p0LVZMT1hhcDhqUWh0ZXpOWGlZWEZkcHZYbUo2VGNZZDVTYlJLZnN6VnBEWHROWTdRTDYwbFhSSkc1T1BSbkEwQjl2LWZPUXhZUTNGa3VmbkpCNmdhUQ==" | base64 -d
eyJhbGciOiJSUzI1NiIsImtpZCI6ImpJcXdDOFMzRk5TaGpEdEhidy1vM0p0bFRuYnJFQzJYVXY2dzM1LUx4Q28ifQ.eyJpc3MiOiJrdWJlcm5ldGVzL3NlcnZpY2VhY2NvdW50Iiwia3ViZXJuZXRlcy5pby9zZXJ2aWNlYWNjb3VudC9uYW1lc3BhY2UiOiJrdWJlLXN5c3RlbSIsImt1YmVybmV0ZXMuaW8vc2VydmljZWFjY291bnQvc2VjcmV0Lm5hbWUiOiJkZWZhdWx0LXRva2VuLTdzcnA3Iiwia3ViZXJuZXRlcy5pby9zZXJ2aWNlYWNjb3VudC9zZXJ2aWNlLWFjY291bnQubmFtZSI6ImRlZmF1bHQiLCJrdWJlcm5ldGVzLmlvL3NlcnZpY2VhY2NvdW50L3NlcnZpY2UtYWNjb3VudC51aWQiOiI2MGJhMzhkZS1jNDQxLTRmYTgtOWYyOC1kNTllNDQyMzk3MWIiLCJzdWIiOiJzeXN0ZW06c2VydmljZWFjY291bnQ6a3ViZS1zeXN0ZW06ZGVmYXVsdCJ9.B9jFIBfhWtiMJjRiz0bV67EwTiOo4G6ZjPp80kZej9BajZWg5FAPNMpEKThEzTqhlbdDWCxbRAV2Ktep1THFr8LPE4VFGEYpY6hp4b1SeDQHcUShZTfBgy9X9xVkYDN666DxRL7fXPY6Ay0W7ZTEz_Q3sOW7rQKnnGlhB-7SfPI7WRx9IiVarRdzuCbl1Rvjl386g67ZVr73pWNmeARslXLP6AzpqTAx5qvXWz6An5_cz1Tby5UM689BXbKMIfWjt-VLOXap8jQhtezNXiYXFdpvXmJ6TcYd5SbRKfszVpDXtNY7QL60lXRJG5OPRnA0B9v-fOQxYQ3FkufnJB6gaQ
USERNAME@PCNAME MINGW64 ~
$ kubectl proxy
Starting to serve on 127.0.0.1:8001




#############another CMD###############
USERNAME@PCNAME MINGW64 ~
$ kubectl.exe run web --image=nginx:latest
pod/web created

USERNAME@PCNAME MINGW64 ~
$ kubectl.exe get pods
NAME   READY   STATUS              RESTARTS   AGE
web    0/1     ContainerCreating   0          26s


USERNAME@PCNAME MINGW64 ~
$ kubectl.exe get pods
NAME   READY   STATUS    RESTARTS   AGE
web    1/1     Running   0          69s




USERNAME@PCNAME MINGW64 ~
$ minikube.exe ssh
                         _             _
            _         _ ( )           ( )
  ___ ___  (_)  ___  (_)| |/')  _   _ | |_      __
/' _ ` _ `\| |/' _ `\| || , <  ( ) ( )| '_`\  /'__`\
| ( ) ( ) || || ( ) || || |\`\ | (_) || |_) )(  ___/
(_) (_) (_)(_)(_) (_)(_)(_) (_)`\___/'(_,__/'`\____)

$ docker container ls
docker container ls
CONTAINER ID   IMAGE                                      COMMAND                  CREATED         STATUS         PORTS     NAMES
2aefd7b6d614   nginx                                      "/docker-entrypoint.тАж"   5 minutes ago   Up 5 minutes             k8s_web_web_default_44044876-debf-48f5-92a0-34f09bfb7b1d_0
d70d994d4ee7   k8s.gcr.io/pause:3.5                       "/pause"                 6 minutes ago   Up 6 minutes             k8s_POD_web_default_44044876-debf-48f5-92a0-34f09bfb7b1d_0
2aca02a7fc31   k8s.gcr.io/metrics-server/metrics-server   "/metrics-server --cтАж"   4 hours ago     Up 4 hours               k8s_metrics-server_metrics-server-7b9c4d7fd9-5tn5j_kube-system_1a64817b-5b39-41b9-b5e8-999e72daa310_0
64cca349ad78   k8s.gcr.io/pause:3.5                       "/pause"                 4 hours ago     Up 4 hours               k8s_POD_metrics-server-7b9c4d7fd9-5tn5j_kube-system_1a64817b-5b39-41b9-b5e8-999e72daa310_0
6fc263c55329   kubernetesui/metrics-scraper               "/metrics-sidecar"       4 hours ago     Up 4 hours               k8s_dashboard-metrics-scraper_dashboard-metrics-scraper-856586f554-w9scc_kubernetes-dashboard_f7a9264d-6f36-4f98-9fe2-69e74895eb49_0
bee1adde446a   kubernetesui/dashboard                     "/dashboard --insecuтАж"   4 hours ago     Up 4 hours               k8s_kubernetes-dashboard_kubernetes-dashboard-67484c44f6-5vgm6_kubernetes-dashboard_89f843e6-53f6-4962-867f-6553162cff9b_0
83bba85f6f1c   k8s.gcr.io/pause:3.5                       "/pause"                 4 hours ago     Up 4 hours               k8s_POD_dashboard-metrics-scraper-856586f554-w9scc_kubernetes-dashboard_f7a9264d-6f36-4f98-9fe2-69e74895eb49_0
c62d62330d67   k8s.gcr.io/pause:3.5                       "/pause"                 4 hours ago     Up 4 hours               k8s_POD_kubernetes-dashboard-67484c44f6-5vgm6_kubernetes-dashboard_89f843e6-53f6-4962-867f-6553162cff9b_0
b3c424603ac9   6e38f40d628d                               "/storage-provisioner"   4 hours ago     Up 4 hours               k8s_storage-provisioner_storage-provisioner_kube-system_57e0a854-01b1-4d1e-a2a5-b0b67e4fb703_1
30b600da4876   8d147537fb7d                               "/coredns -conf /etcтАж"   4 hours ago     Up 4 hours               k8s_coredns_coredns-78fcd69978-gnwbl_kube-system_8abeb268-aca7-49e8-adab-fed4cc488ea1_0
2e591cfa672c   873127efbc8a                               "/usr/local/bin/kubeтАж"   4 hours ago     Up 4 hours               k8s_kube-proxy_kube-proxy-dtzqd_kube-system_e89428bb-69d7-417e-96ca-e704b17abbf4_0
bea560983b8b   k8s.gcr.io/pause:3.5                       "/pause"                 4 hours ago     Up 4 hours               k8s_POD_coredns-78fcd69978-gnwbl_kube-system_8abeb268-aca7-49e8-adab-fed4cc488ea1_0
b3c3bca74575   k8s.gcr.io/pause:3.5                       "/pause"                 4 hours ago     Up 4 hours               k8s_POD_kube-proxy-dtzqd_kube-system_e89428bb-69d7-417e-96ca-e704b17abbf4_0
cdb252221d6b   k8s.gcr.io/pause:3.5                       "/pause"                 4 hours ago     Up 4 hours               k8s_POD_storage-provisioner_kube-system_57e0a854-01b1-4d1e-a2a5-b0b67e4fb703_0
a5d474d64f08   b51ddc1014b0                               "kube-scheduler --auтАж"   4 hours ago     Up 4 hours               k8s_kube-scheduler_kube-scheduler-minikube_kube-system_97bca4cd66281ad2157a6a68956c4fa5_0
b871c280509d   004811815584                               "etcd --advertise-clтАж"   4 hours ago     Up 4 hours               k8s_etcd_etcd-minikube_kube-system_8df34c120e5b6d8e2965e940214cdfa2_0
29f7df7b1b75   5425bcbd23c5                               "kube-controller-manтАж"   4 hours ago     Up 4 hours               k8s_kube-controller-manager_kube-controller-manager-minikube_kube-system_20326866d8a92c47afe958577e1a8179_0
3ab039320995   e64579b7d886                               "kube-apiserver --adтАж"   4 hours ago     Up 4 hours               k8s_kube-apiserver_kube-apiserver-minikube_kube-system_8fef46ac84946d4981cc2a7e66df8e01_0
813c0fa36d08   k8s.gcr.io/pause:3.5                       "/pause"                 4 hours ago     Up 4 hours               k8s_POD_kube-scheduler-minikube_kube-system_97bca4cd66281ad2157a6a68956c4fa5_0
1c9e4d1e68db   k8s.gcr.io/pause:3.5                       "/pause"                 4 hours ago     Up 4 hours               k8s_POD_kube-controller-manager-minikube_kube-system_20326866d8a92c47afe958577e1a8179_0
1bb037e7becf   k8s.gcr.io/pause:3.5                       "/pause"                 4 hours ago     Up 4 hours               k8s_POD_kube-apiserver-minikube_kube-system_8fef46ac84946d4981cc2a7e66df8e01_0
fe88ba73c271   k8s.gcr.io/pause:3.5                       "/pause"                 4 hours ago     Up 4 hours               k8s_POD_etcd-minikube_kube-system_8df34c120e5b6d8e2965e940214cdfa2_0
$


USERNAME@PCNAME MINGW64 ~
$ kubectl apply -f pod.yaml
pod/nginx created

USERNAME@PCNAME MINGW64 ~
$ kubectl apply -f rs.yaml
replicaset.apps/webreplica created


USERNAME@PCNAME MINGW64 ~
$ kubectl.exe get rs
NAME         DESIRED   CURRENT   READY   AGE
webreplica   2         2         2       14s

USERNAME@PCNAME MINGW64 ~
$ kubectl.exe get pod
NAME               READY   STATUS    RESTARTS   AGE
nginx              1/1     Running   0          30s
web                1/1     Running   0          10m
webreplica-lvs5p   1/1     Running   0          21s
webreplica-lwcxd   1/1     Running   0          21s

USERNAME@PCNAME MINGW64 ~
$

USERNAME@PCNAME MINGW64 ~
$ kubectl.exe delete pod webreplica-lwcxd
pod "webreplica-lwcxd" deleted

USERNAME@PCNAME MINGW64 ~
$ kubectl.exe get pod
NAME               READY   STATUS              RESTARTS   AGE
nginx              1/1     Running             0          3m26s
web                1/1     Running             0          13m
webreplica-lvs5p   1/1     Running             0          3m17s
webreplica-twszs   0/1     ContainerCreating   0          2s

USERNAME@PCNAME MINGW64 ~
$ kubectl.exe get pod
NAME               READY   STATUS    RESTARTS   AGE
nginx              1/1     Running   0          3m33s
web                1/1     Running   0          13m
webreplica-lvs5p   1/1     Running   0          3m24s
webreplica-twszs   1/1     Running   0          9s

USERNAME@PCNAME MINGW64 ~
$

