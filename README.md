# Extension scenarios for data capture

This accelerator project supports below extension scenarios using existing [Data capture capability in Microsoft Sustainability Manager](https://learn.microsoft.com/en-us/industry/sustainability/record-data-capture)

## Scenario-1: Support bulk import

In data capture, users can use the built-in user interface to upload their files associated to their document request. This extension scenario supports end users to upload all their utility bills to a sharepoint site folder where the automation will process those documents and create and submit each file to data capture functionality

<img width="578" alt="image" src="https://github.com/user-attachments/assets/2c1af6c0-c0ab-461f-91ad-42a4d91d490b" />

## How to deploy the accelerator

### Pre-Requisites

1. A sharepoint site and folder where folders will be uploaded
2. A subfolder where processed files will be moved after documents are processed a structure like below

   <img width="283" alt="image" src="https://github.com/user-attachments/assets/a5da5bea-c814-44bb-972b-d55323dab998" />


### Deployment steps

1. Download the managed solution provided under this code repository
2. Go to [PowerApps Maker Portal](https://make.powerapps.com) and select solutions, then import solution and select the solution.zip file.
3. Define Dataverse and SharePoint connections and Select Next

   <img width="677" alt="image" src="https://github.com/user-attachments/assets/13cbadd0-87fb-4f2c-a999-7c2b92b7e639" />

4.
