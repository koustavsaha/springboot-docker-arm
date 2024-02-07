This directory contains a Tekton pipeline for this springboot app
**Prereq**
# A ConfigMap to hold the maven-settings.xml which is required by `maven` Task
kubectl create cm maven-settings --from-file=settings.xml=Resources/maven-settings.xml 

Use Pipeline SA 
Don't use default branch
