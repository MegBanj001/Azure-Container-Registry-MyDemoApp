![Result](https://github.com/user-attachments/assets/4fa6d9b1-ed77-449e-9e2d-f3fadf34092b)

In this project, I did the following things to achieve my desired result.

a. Containerize an application

b. Create an Azure Registry and Container Instance

c. Build a Docker image and push it to Azure

d. Deploy the image to Azure Container Service


-Create a file named index.html where you would save the codes for your app. After that has been done, create another file named dockerfile, here you would save your command to build your docker image.

-Log in your Azure account and create a Container Registry

-Create a Resource Group if you don’t have one already and give your registry a name. My Container Registry successfully deployed. Take note of the Login Server information as it is needed to build your docker image.

-Go to Settings, click Access Keys and Activate the Admin User.
You need to activate the Admin user to be able to create an Azure Container Instances. After you have done this, it is time to go build the docker image.

-Go to VS code, open a Terminal and type az login . az login helps you login to your azure account.
After successfully logging into your Azure account, you type az acr login —name <the name of your azure container registry>. 
When that has been successful, you go ahead and build your docker image by running, docker build . -t <login server info>/<name of the image you want to create:latest>

-I pushed the image I had created to Azure so that I can use it. For that purpose, I ran the docker push command. docker push <login server info>/<image name>

-Confirmed my image had been sucessfully pushed to Azure by opening my Container Registry, clicked on Services, then Repositories and voila, my image has been pushed to my Azure Container Registry.

-Create a Container Instance. Choose your Resource Group, give the container instance a name.

-For image source, choose the container registry earlier created. Choose your Registry and choose your Image from the drop-down menu. Click Create.

-After successful deployment, I went ahead and copied the Public IP address.

-Opened a new tab, pasted and ran the public ip adddress.

-App opened.
