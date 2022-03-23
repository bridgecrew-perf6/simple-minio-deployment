# simple-minio-deployment
Repo to store the minimal required yaml files to deploy minio at an OCP cluster

# TL;DR;

````bash
oc apply -f yaml/minio-ns.yaml
sleep 2
oc apply -f yaml/.
````

# Obtain the WEBUI and API routes

````bash
oc get route minio-webui -n minio -o 'jsonpath={..spec.host}' && \
echo "" && \
oc get route minio-api -n minio -o 'jsonpath={..spec.host}' && \
echo ""
````
