```
mkdir helloworld-go
cd helloworld-go

go mod init helloworld-go

gcloud auth login

export PROJECT_ID=xxxx

gcloud builds submit --tag gcr.io/$PROJECT_ID/helloworld-go-github

gcloud run deploy --image gcr.io/$PROJECT_ID/helloworld-go-github --platform managed


git tag -a prod-v1.0.0 -m 'release version 1.0.0'

git push origin --tags

```