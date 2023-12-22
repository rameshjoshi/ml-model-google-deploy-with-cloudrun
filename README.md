**scenario**
take advantage of the power and availability of cloud computing when making predictions from their trained ML models. You have been asked to take a pre-trained model and deploy it to Cloud Run for testing purposes.

**Resources**
Cloud Build API, Cloud Run API, ml model

**Design Flow** :  --> 
You have **pretrained** tensorflow model saved in development storage, you use **cloud build** to build containerized image (docker) and saved in google **container registry** (gcr.io). The build image is then deploy into **cloud run** service with accessable endpoint. Then use endpoint to test ML predictition.
![image](https://github.com/rameshjoshi/ml-model-google-deploy-with-cloudrun/assets/7277702/206d987a-a033-4df5-bfc4-f629dcc7a3a7)




**Cloud Build Overview** : -->
Cloud Build, Google Cloud’s continuous integration (CI) and continuous delivery (CD) platform, lets you build software quickly across all languages. Get complete control over defining custom workflows for building, testing, and deploying across multiple environments such as VMs, serverless, Kubernetes, or Firebase.


**Cloud Run Overview** : -->
Cloud Run is a managed compute platform that lets you run containers directly on top of Google's scalable infrastructure.

You can deploy code written in any programming language on Cloud Run if you can build a container image from it. In fact, building container images is optional. If you're using Go, Node.js, Python, Java, .NET Core, or Ruby, you can use the source-based deployment option that builds the container for you, using the best practices for the language you're using.

