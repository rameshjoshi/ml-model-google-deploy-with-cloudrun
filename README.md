**Scenario**
take advantage of the power and availability of cloud computing when making predictions from their trained ML models. You have been asked to take a pre-trained model and deploy it to Cloud Run for testing purposes.

**Resources**
Cloud Build API, Cloud Run API, ml model

**Design Flow** :  --> 
You have **pretrained** tensorflow model saved in development storage, you use **cloud build** to build containerized image (docker) and saved in google **container registry** (gcr.io). The build image is then deploy into **cloud run** service with accessable endpoint. Then use endpoint to test ML predictition.
![image](https://github.com/rameshjoshi/ml-model-google-deploy-with-cloudrun/assets/7277702/206d987a-a033-4df5-bfc4-f629dcc7a3a7)




**Cloud Build Overview** : -->
Cloud Build, Google Cloud’s continuous integration (CI) and continuous delivery (CD) platform, lets you build software quickly across all languages. Get complete control over defining custom workflows for building, testing, and deploying across multiple environments such as VMs, serverless, Kubernetes, or Firebase.

    1. Invoke the Cloud Build service to create the container and store it in Container Registry
    $gcloud builds submit --tag gcr.io/playground-s-11-a75f0616/index
    ![image](https://github.com/rameshjoshi/ml-model-google-deploy-with-cloudrun/assets/7277702/53740024-d511-4c03-8aed-4e57221936dc)
**Containerize the App and Store the Disk Image** : 
    project_id = playground-s-11-a75f0616
    
    1. Invoke the Cloud Build service to create the container and store it in Container Registry
    $gcloud builds submit --tag gcr.io/playground-s-11-a75f0616/index
    ![image](https://github.com/rameshjoshi/ml-model-google-deploy-with-cloudrun/assets/7277702/53740024-d511-4c03-8aed-4e57221936dc)

    2. Deploy the containerized image to Cloud Run
    $gcloud run deploy --image=gcr.io/playground-s-11-a75f0616/index --platform managed

    ![image](https://github.com/rameshjoshi/ml-model-google-deploy-with-cloudrun/assets/7277702/0875fec8-493e-4fc3-b32f-858a1b49406d)
    ![image](https://github.com/rameshjoshi/ml-model-google-deploy-with-cloudrun/assets/7277702/2d264f0c-ae53-4255-af59-5831be2636b4)



**Cloud Run Overview** : -->
Cloud Run is a managed compute platform that lets you run containers directly on top of Google's scalable infrastructure.

You can deploy code written in any programming language on Cloud Run if you can build a container image from it. In fact, building container images is optional. If you're using Go, Node.js, Python, Java, .NET Core, or Ruby, you can use the source-based deployment option that builds the container for you, using the best practices for the language you're using.


