# go-web-app-devopsified
WE ARE GOING TO CONTAINERIZING THE PROJECT, FOR THAT WE ARE GOING TO WRITE A DOCKERFILE THROUGH WHICH WE ARE GOING TO CREATE IMAGE 
THEN WE ARE GOING TO CREATE KUBERNETES SUCH AS DEPLOYMENT,SERVICE AND INGRESS
THEN WE WILL DO CONTINUOUS INTEGRATION, WE WILL USE GITHUB ACTION TO IMPLEMENT THE CI
THEN WE WILL IMPLEMENT CONTINUOUS DELIVERY FOR THAT WE WILL USE GITOPS(ARGO CD)
THEN WE WILL CREATE KUBERNETES CLUSTER BECAUSE CI/CD HAS TO DEPLOY APPLICATION ON TARGET PLATFORM AND THE TARGET PLATFORM WILL BE KUBERNETES CLUSTER FOR THAT WE WILL USE EKS
WE WILL ALSO SETUP HELM CHART FOR THE APPLICATION
WE WILL ALSO SET AN INGRESS CONTROLLER. SO, THAT THE INGRESS CONTROLLER WOULD CREATE A LOAD BALANCER DEPENDING ON INGRESS CONFIGURATION.SO, THAT THE APPLICATION CAN BE EXPOSED TO THE OUTSIDE WORLD
After containerization a application , push the image into dockerhub because kubernetes cluster try pullout image from dockerhub
Ingress controller watches ingress resources and create loadbalancer
Chart.yml provides the information of the chart you can assume it as the metadata.So,it provides the information of the chart
For CI i am using GH actions and for CD i am using Gitops/ArgoCD
CI/CD PIPELINE FLOW
CI - Stage1:Build and unit test ,Stage2:Static code analysis,Stage3:Docker image creation and pushing the docker image, Stage4:Upadat helm
CD - In CD ,we will use ArgoCD .Argocd will watch the helm chart. When ever the values.yml is updated it will pull the helm chart and install it in kubernetes cluster
