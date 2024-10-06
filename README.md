 # Deploy-Azure-WebApp

## Objective

The Deploy-Azure-WebApp project aimed to deploy a simple web application using Azure App Service. The main goal was to gain hands-on experience in setting up cloud infrastructure, deploying web apps, and understanding key Azure services. This project provided a practical foundation in cloud security and web app deployment.

### Skills Learned

- Understanding of Azure App Service and its deployment process.
- Knowledge of Azure resource groups, App Service Plans, and web app configurations.
- Ability to deploy code to cloud-based environments.
- Familiarity with basic cloud networking concepts (e.g., scaling, regions).
- Practical exposure to Azure Portal and Cloud Shell tools.

### Tools Used

- Azure Portal for managing cloud resources and deployments.
- Azure Cloud Shell for executing CLI commands.
- Git for cloning repositories and deploying web apps.
- Azure App Service for hosting the web application.

## Steps

- Step 1: Create Resource group

  A resource group is a container that holds related resources for an Azure solution.
 1.1 We can go ahead and create a resource group. 
![image](https://github.com/user-attachments/assets/dcb389e7-6319-45ce-bbbb-155ee8b78782)
1.2 After creating the resource group we can see it under Resources in home.
![image](https://github.com/user-attachments/assets/50a40c96-1af7-4ed9-b6f6-ac5b98b73be9)

- Step 2: Create an App Service Plan
An App Service Plan defines the compute resources for an app.

2.1 Navigate to App services
2.2 Create a New Web App Service Plan
2.2.1 Select Subscription
2.2.2 Select the Resource group we created in Step 1
2.2.3 We'll enter a unique name for our app: MyPersWebapp
2.2.4 In Runtime Stack we'll select .NET 6
2.2.5 Keep the region the same as our resource group
![image](https://github.com/user-attachments/assets/691cf112-7d6e-435d-b7b2-2c2688e236e3)
2.2.6 Review and create the App Service plan

- Step 3: Deploy a Sample Web App
  Now that the App Service is set up, we can deploy a sample application.
  
  3.1 Once deployment of the app services is complete click on go to resource
  3.2 Click on Browse in the top corner to see the default Web Page
  ![image](https://github.com/user-attachments/assets/e726cc67-5b1d-40b0-99dc-f44e068f90ee)

- Step 4:  Deploy Code to Your Web App
  We can deploy our own code or use sample code, in this case we will use sample code.
  Open Azure Cloud Shell:

  4.1 Click on the Cloud Shell icon (terminal icon) in the top navigation bar.
  4.1.1 Choose "Bash" if prompted and select subscription. A shell will spawn.
  ![image](https://github.com/user-attachments/assets/e7ac4315-abee-4f06-8dca-e98355bd20aa)

  4.2 Clone a Sample App (git clone https://github.com/Azure-Samples/html-docs-hello-world)
  ![image](https://github.com/user-attachments/assets/26ac1e41-951f-45a8-a871-ddf43089a238)

  4.3 Navigate to the cloned directory (cd html-docs-hello-world)
  4.4 Zip the contents (zip -r app.zip .)
  ![image](https://github.com/user-attachments/assets/7d73172b-9d08-4ef7-9140-2d6ad6dcc847)

  4.5 Deploy using az webapp (az webapp deployment source config-zip --resource-group MyResourceGrp --name MyPersWebapp --src app.zip)
  ![image](https://github.com/user-attachments/assets/0f3eaeee-e9f1-49a4-bfd0-c543143eb99f)
  4.6 Click on Browse in app services intance we created and now we should see our sample page running
  ![image](https://github.com/user-attachments/assets/1c7e3948-d3d5-4a0f-b7b0-e52f6879cd86)
