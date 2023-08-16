## Retrieve pods

This YAML configuration is based on modifications made to the example provided in the [Kubernetes documentation](https://kubernetes.io/docs/tasks/run-application/access-api-from-pod/):

Firstly, to enable the Pod to retrieve information about all pods in the default namespace, it is necessary to grant the Pod permissions to perform list and get operations. To achieve this, a Role is created and then bound to the existing service account in the default namespace.

Next, to use curl for retrieving pod information, an image containing curl is employed. This image is configured with the necessary components, including the certificate file, service account token, and API server URL. This configuration is defined within the YAML between lines 14 and 20.
