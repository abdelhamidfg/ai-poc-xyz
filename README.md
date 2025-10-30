## Prerequisites

- A **Data Science Project** in RHOAI.
- MinIO reachable from your project (Service/Route), with **access key/secret**.
 
---


## Create an S3 Connection to MinIO
Create the S3 Connection (UI)
	-	In the RHOAI Dashboard, open your Data Science Project → Connections → Create connection.
	-	Connection type: S3 compatible object storage – v1
	-	Fill the form (adapt values to your cluster):
	•	Connection name: s3-minio
	•	Resource name: s3-minio
	•	Access key: myaccesskey
	•	Secret key: mysecretkey
	•	Endpoint: http://minio-service.minio.svc.cluster.local:9000
Include the protocol (http:// or https://) here. For MinIO on port 9000, it’s typically HTTP.
	•	Region: (leave blank) or us-east-1
	•	Bucket: pipelines
	4.	Click Create.
