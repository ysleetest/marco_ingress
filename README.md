
# FortiWeb Ingress Controller

# Deployment

## Get Repo Information
   

    helm repo add fwb-ingress-controller https://ysleetest.github.io/marco_ingress/

    helm repo update

   ## Install FortiWeb Ingress Controller
   :warning: Before install, you have to create the image pull secret under the specified namespace fortiweb-ingress.

    helm install first-release --namespace fortiweb-ingress fortiweb-ingress-controller/fwb-k8s-ctrl-new

## Check the installation

    helm history -n fortiweb-ingress first-release
    
    kubectl get -n fortiweb-ingress deployments
    
    kubectl get -n fortiweb-ingress pods
 
## Upgrading chart

    helm repo update
    helm upgrade -n fortiweb-ingress first-release fortiweb-ingress-controller/fwb-k8s-ctrl-new

## Uninstall Chart

    helm uninstall -n fortiweb-ingress first-release
