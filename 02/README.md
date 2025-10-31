## Prerequisites

- A **Data Science Project** in RHOAI.
- MinIO reachable from your project (Service/Route), with **access key/secret**.

 
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

## Create a new workbench
![S3 connection form](/images/ingestion-wb.jpg) 
