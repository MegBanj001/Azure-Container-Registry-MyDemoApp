![Result](https://github.com/user-attachments/assets/4fa6d9b1-ed77-449e-9e2d-f3fadf34092b)

In this project, I did the following things to achieve my desired result.

a. Containerized an application

b. Created an Azure Registry and Container Instance

c. Built a Docker image and pushed it to Azure

d. Deployed the image to Azure Container Service


STEPS I TOOK:

-Created a file named index.html where I savedthe codes for my app. After that was done, I created another file named dockerfile, here I saved my command to build my docker image.

-Logged into my Azure account and created a Container Registry.

-Created a Resource Group and gave my registry a name. My Container Registry successfully deployed. Took note of the Login Server information as it would be needed to build my docker image.

-Went to Settings, clicked Access Keys and Activated the Admin User.
The Admin user needed to be activated to enable me create an Azure Container Instances. After that was done, it was time to go build the docker image.

-Went to VS code, opened a Terminal and typed az login. az login helps you login to your azure account.
After successfully logging into my Azure account, I typed az acr login —name <the name of your azure container registry>. 
When that has been successful, I went ahead to build my docker image by running, docker build . -t <login server info>/<name of the image you want to create:latest>

-I pushed the image I had created to Azure so that I can use it. For that purpose, I ran the docker push command. docker push <login server info>/<image name>

-Confirmed my image had been sucessfully pushed to Azure by opening my Container Registry, clicked on Services, then Repositories and voila, my image has been pushed to my Azure Container Registry.

-Created a Container Instance. Chose my Resource Group, gave the container instance a name.

-For image source, I chose the container registry earlier created. Chose my Registry and chose my Image from the drop-down menu. Clicked Create.

-After successful deployment, I went ahead and copied the Public IP address.

-Opened a new tab, pasted and ran the public ip adddress.

-App opened.
