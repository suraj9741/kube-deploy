# Detail of this repo
- In this repository stored 
  - [ansible script](#ansible-script) 
  - [k8s manifest file](#k8s-manifest-file) 
  - [helm chart](#helm-chart) 
---
## ansible script
- In ansible script below task will perform 
  - Clone this repo
  - Change Image tag in manifest file `( we are not using this file for deploy just for understand and if deployment fails backup will be there )`
  - helm chart is already present in repo at [mychart location](mychart) so at the deployment time we are passing image tag to helm and upgrading helm so new image will deploy in k8s cluster 
  - take look on [code](ansible/update_manifestfile/deploy.yml)
---
## k8s manifest file
- In [k8s](k8s) directory we wrote a deployment and service file like that same we created helm chart
---
## Helm chart
- All Helm charts are available in [mychart](mychart) directory.
- Configured all details inside [value](mychart/values.yaml) file as per deployment. 