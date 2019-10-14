# CodeStream Pipeline Monitoring
This demo showcase how Ms Apps could be deployed in CI/CD Fashion on any K8 cluster and have KPIs monitored automatically by vROPs and WaveFront

# Requerimients

1.- Kubernetes Cluster
 
	Any reachable Kubernetes cluster, at least a Master and a worker, this demo has been tested with K8 v1.12.9 on Cloud PKS,it is assumed that kubeclt is configured and you can deploy apps stand-alone.
  
   ![K8-Cluster](media/kubernetes-cluster.png)
  
2.- vROPs and VMware vRealize Operations Management Pack for Container Monitoring
 
	This demo has been tested with vROPs 7.5 and vRealize Operations Management Pack for Container Monitoring version 1.14.1 and assumes that they have been installed, however instructions below are provided to integrate vROPs with K8.
  
  ![vrops](https://github.com/moffzilla/usps-central-sddc-se/blob/master/media/vrops.png)
  
3.- Wavefront
 
	This demo has been tested with Wavefront by [ VMware Sandbox ](https://vmware.wavefront.com/) and assumes it is configured and ready, however instructions below are provided to integrate Wavefront with K8.

![Wavefront](media/wavefront.png)
  
4.- vRealize Automation
 
	This demo has been tested with vRealize Automation Cloud but it can work with vRealize Automation 8.0 and this demo assumes that the basic configuration has been complete and basic blueprints can be deployed and Code Stream is functional, e.g. Cloud Zones, Projects, Profiles, etc, however instructions below are provided for integrating K8 and blueprints. 
  
  ![vRA](media/vRA-k8.png)
  
# Integration Instructions

1.- Kubernetes Cluster to vROPs
 
	Any reachable Kubernetes cluster, at least a Master and a worker, this demo has been tested with K8 v1.12.9 on Cloud PKS,it is assumed that kubeclt is configured and you can deploy apps stand-alone.
  
2.- Kubernetes Cluster to Wavefront
 
	Any reachable Kubernetes cluster, at least a Master and a worker, this demo has been tested with K8 v1.12.9 on Cloud PKS,it is assumed that kubeclt is configured and you can deploy apps stand-alone.
  
3.- Kubernetes Cluster to vRealize Automation 
 
	Any reachable Kubernetes cluster, at least a Master and a worker, this demo has been tested with K8 v1.12.9 on Cloud PKS,it is assumed that kubeclt is configured and you can deploy apps stand-alone.
  
# Demo Instructions

The section below provides the general steps to demo

1.- Log in to vRealize Automation and go to Code Stream
 
	Any reachable Kubernetes cluster, at least a Master and a worker, this demo has been tested with K8 v1.12.9 on Cloud PKS,it is assumed that kubeclt is configured and you can deploy apps stand-alone.
