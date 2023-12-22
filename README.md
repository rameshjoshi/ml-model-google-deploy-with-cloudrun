**scenario**
take advantage of the power and availability of cloud computing when making predictions from their trained ML models. You have been asked to take a pre-trained model and deploy it to Cloud Run for testing purposes.

**Resources**
Cloud Build API, Cloud Run API, ml model

****Design Flow****

You have **pretrained** saved tensorflow model, you use **cloud build** to build containerized image (docker) and saved in google **container registry** (gcr.io). The build image is then deploy into **cloud run** service with accessable endpoint. Then use endpoint to test ML predictition.
![image](https://github.com/rameshjoshi/ml-model-google-deploy-with-cloudrun/assets/7277702/206d987a-a033-4df5-bfc4-f629dcc7a3a7)

