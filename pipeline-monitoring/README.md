# CodeStream Pipeline Monitoring
This demo showcase how Ms Apps could be deployed in CI/CD Fashion on any K8 cluster and have KPIs monitored automatically by vROPs and WaveFront

# Requerimients

1.- Kubernetes Cluster
 
	Any reachable Kubernetes cluster, at least one Master and one worker, 
	this demo has been tested with K8 v1.12.9 on Cloud PKS,
	it is assumed that kubeclt is configured and you can deploy apps stand-alone.
  
   ![K8-Cluster](https://github.com/moffzilla/usps-central-sddc-se/blob/master/media/kubernetes-cluster.png)
  
2.- vROPs and VMware vRealize Operations Management Pack for Container Monitoring (https://marketplace.vmware.com/vsx/solutions/vrealize-operations-management-pack-for-container-monitoring?ref=search#summary)
 
	This demo has been tested with vROPs 7.5 and vRealize Operations Management Pack 
	for Container Monitoring version 1.14.1 and assumes that they have been installed, 
	however instructions below are provided to integrate vROPs with K8.
  
  ![vrops](https://github.com/moffzilla/usps-central-sddc-se/blob/master/media/vrops.png)
  
3.- Wavefront
 
	This demo has been tested with Wavefront by VMware Sandbox https://vmware.wavefront.com/ 
	and assumes it is configured and ready, however instructions below are provided to integrate Wavefront with K8.

![Wavefront](https://github.com/moffzilla/usps-central-sddc-se/blob/master/media/wavefront.png)
  
4.- vRealize Automation
 
	This demo has been tested with vRealize Automation Cloud but it can work with vRealize Automation 8.0
	It is assumed that the basic configuration has been complete and basic blueprints can be deployed 
	and Code Stream is functional, e.g. Cloud Zones, Projects, Profiles, etc, however instructions below 
	are provided for integrating K8 and blueprints. 
  
  ![vRA](https://github.com/moffzilla/usps-central-sddc-se/blob/master/media/vRA-k8.png)
  
# Integration Instructions

1.- Kubernetes Cluster to vROPs
 
	A deamon set is deployed at the Kubernetes cluster for vROPs able to connect and pull KPI data from the cluster.
	Instructions for configuring vROPs can be found here: 
	https://docs.vmware.com/en/Management-Packs-for-vRealize-Operations-Manager/1.4.1/container-monitoring/GUID-87AEB0B9-EB85-4DDC-AD31-1AEE1179C4B4.html
	
	A sample of the deamon set can be found here:
	xxxxx
	
	Example:
	![Connection Sample](https://github.com/moffzilla/usps-central-sddc-se/blob/master/media/vrops-k8-connection-sample.png)
	
	After accepting the certificate there is a warning, just accept and save.
	wait for a few minutes so vROPs can connect and start collecting
	![vrops-k8-collecting](https://github.com/moffzilla/usps-central-sddc-se/blob/master/media/vrops-k8-collecting.png)
	
	At this point you can access the Kubernetes Overview Dashboard and see any KPI related to any pre-deployed POD, namespaces, etc.
  
2.- Kubernetes Cluster to Wavefront
 
	Instructions for configuring Wavefront to Kubernetes can be found here:
	https://vmware.wavefront.com/integration/kubernetes/setup
	Please note that the API will be required but normally the documentation itself shows it
	Basically a DeamonSet is deployed at the cluster level and samples can be found here:  
	xxxxxxx
	After that you can access the default dashboards and you should be able to collect and see any KPI related to any pre-deployed POD, namespaces, etc.

  
3.- Kubernetes Cluster to vRealize Automation 
 
	Any reachable Kubernetes cluster, at least a Master and a worker, 
	this demo has been tested with K8 v1.12.9 on Cloud PKS,
	it is assumed that kubeclt is configured and you can deploy apps stand-alone.
  
# Demo Instructions

The section below provides the general steps to demo

1.- Log in to vRealize Automation and go to Code Stream
 
	Any reachable Kubernetes cluster, at least a Master and a worker, 
	this demo has been tested with K8 v1.12.9 on Cloud PKS,
	it is assumed that kubeclt is configured and you can deploy apps stand-alone.
