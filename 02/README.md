## Prerequisites

- A **Data Science Project** in RHOAI.
- MinIO reachable from your project (Service/Route), with **access key/secret**.
-  upload data.zip folder into a folder with name data in the s3 bucket

 
---

## Create a Secret for storing S3 connection for the pipeline
### Example: OpenShift Secret Definition

```yaml
apiVersion: v1
kind: Secret
metadata:
  name: aws-connection-s3-minio
type: Opaque
stringData:
  AWS_S3_ENDPOINT: "http://minio-service.minio.svc.cluster.local:9000"
  AWS_ACCESS_KEY_ID: "myaccesskey"
  AWS_SECRET_ACCESS_KEY: "mysecretkey"
  AWS_S3_BUCKET: "pipelines"
```
## Create a new workbench

![workbench](/images/2-ingestion-wb.jpg) 
![workbench](/images/gpu-wb-attach-connection.jpg) 

