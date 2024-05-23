# Azure OpenAI and Azure Search Integration  
  
This project demonstrates how to integrate Azure OpenAI with Azure Search using Python. The provided script sets up logging, retrieves necessary credentials from environment variables, and sends a chat completion request to Azure OpenAI.  
  
## Prerequisites  
  
1. **Python 3.7+**: Ensure you have Python installed on your machine.  
2. **Azure Subscription**: You need an active Azure subscription.  
3. **Environment Variables**: Set the following environment variables with appropriate values:  
   - `AZURE_OPENAI_ENDPOINT`  
   - `CHAT_COMPLETIONS_DEPLOYMENT_NAME`  
   - `SEARCH_ENDPOINT`  
   - `SEARCH_INDEX`  
   - `AZURE_SEARCH_API_KEY`  
   - `API_VERSION`  - NOTE this is found in the API docs - the spec i am using is 2024-02-01
  
## Setup  
  
1. **Clone the Repository**:  
   ```sh  
   git clone <repository-url>  
   cd <repository-directory>  

1. **Login into AZ cli for a credential**:  
DefaultAzureCredential is used here, and if you are running locally, ensure you are using a valid credential for this code. Otherwise setup and configure RBAC to system assigned managed identities in OpenAI and Azure Search.

1. **Run the Script**:  
python script.py  


## Deploying Azure Search and Azure OpenAI services involves a series of steps within the Azure Portal. Below are the detailed steps for each service.

### Deploying Azure Cognitive Search
Log in to the Azure Portal:
Navigate to Azure Portal and log in with your Azure account credentials.
Create a new Azure Cognitive Search service:
Click on Create a resource in the left-hand menu.
Search for Azure Cognitive Search and select it from the list.
Click Create.

#### Configure your Search service:
Basics:
Subscription: Select your Azure subscription.
Resource Group: Create a new resource group or select an existing one.
Service Name: Provide a unique name for your search service.
Region: Choose the region where you want to deploy the service.
Pricing Tier: Select a pricing tier based on your needs (e.g., Free, Basic, Standard).
Click Review + create and then Create.
Create a Search Index:
Once the service is created, navigate to the Azure Cognitive Search service in the portal.
Under the Index section, click on New Index.
Define the schema for your index including fields, their types, and other settings.
Click Create to deploy the index.

### Deploying Azure OpenAI Service
Log in to the Azure Portal:
Navigate to Azure Portal and log in with your Azure account credentials.
Create a new Azure OpenAI service:
Click on Create a resource in the left-hand menu.
Search for Azure OpenAI and select it from the list.
Click Create.

#### Configure your OpenAI service:
Basics:
Subscription: Select your Azure subscription.
Resource Group: Create a new resource group or select an existing one.
Region: Choose the region where you want to deploy the service.
Name: Provide a unique name for your OpenAI service.
Pricing Tier: Select a pricing tier based on your needs.
Click Review + create and then Create.
Create a Deployment:
Once the service is created, navigate to the Azure OpenAI service in the portal.
Under the Deployments section, click on New Deployment.
Select a model and configure the deployment settings.
Click Create to deploy the model.