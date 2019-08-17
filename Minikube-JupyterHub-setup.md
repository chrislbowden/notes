# Setting up JupyterHub on Ubuntu and Minikube

## Install kubectl, Minikube and VirtualBox

https://kubernetes.io/docs/tasks/tools/install-kubectl/#install-kubectl-on-linux

https://www.virtualbox.org/wiki/Downloads

https://kubernetes.io/docs/tasks/tools/install-minikube/

## Install Helm and JupyterHub
Follow the JupyterHub install docs to [install Helm](https://zero-to-jupyterhub.readthedocs.io/en/stable/setup-helm.html) and then [install JupyterHub](https://zero-to-jupyterhub.readthedocs.io/en/stable/setup-jupyterhub.html#setup-jupyterhub) 
but use the minikube-config.yaml from the [JupyterHub repo](https://github.com/jupyterhub/zero-to-jupyterhub-k8s/blob/master/minikube-config.yaml).


You can the reach JupyterHub at `http://<minikube ip>:<NodePort>`.

You can get the minikube ip from:
```
minikube ip
```

and the NodePort is defined in minikube-config.yaml.

To [persist notebooks in local storage](https://github.com/jupyterhub/zero-to-jupyterhub-k8s/issues/661) after the notebook server is shut down,
change the storage type to dynamic in minikube-config.yaml.
