`docker build -t app .`  
`docker run -p 8888:80 app`

失敗する

`docker tag app gcr.io/katayama8000/app`  
`docker push gcr.io/katayama8000/app`

成功する

`gcloud run deploy nest-cloudrun --source .`

https://www.youtube.com/watch?v=ZmfDlUAokYc

- サービスアカウントと紐付ける
