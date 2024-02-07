This directory contains a Tekton pipeline for this springboot app
**Prereq**
# A ConfigMap to hold the maven-settings.xml which is required by `maven` Task
kubectl create cm maven-settings --from-file=settings.xml=Resources/maven-settings.xml 

# A dedicated sa for the pipeline
kubectl create sa tekton-pipeline 

# Run this if it's on OpenShift
oc adm policy add-role-to-user edit -z tekton-pipeline 
oc adm policy add-scc-to-user privileged -z tekton-pipeline 
