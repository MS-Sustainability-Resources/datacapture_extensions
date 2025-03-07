# Extension scenarios for data capture

This accelerator project supports below extension scenarios using existing [Data capture capability in Microsoft Sustainability Manager](https://learn.microsoft.com/en-us/industry/sustainability/record-data-capture)

## Scenario-1: Support bulk import

In data capture, users can use the below built-in user interface to define their document request and then upload their file associated to their document request. 

<img width="1199" alt="image" src="https://github.com/user-attachments/assets/100d7255-1261-43ba-b836-815c6e6dc3e4" />

However, currently the user interface doesn't support bulk processing of documents. This extension scenario supports end users to upload all their utility bills to a sharepoint site folder like below

![image](https://github.com/user-attachments/assets/95f4b34c-a4da-4e7b-a956-667110a9384a)

After running the power automate flow as shwon below, 

<img width="1196" alt="image" src="https://github.com/user-attachments/assets/20f3c574-0244-4981-933e-8b525a9ae29c" />

it will create document request record per each file and call the built-in uploadDocument action to submit the file content for processing as shown below 

<img width="578" alt="image" src="https://github.com/user-attachments/assets/2c1af6c0-c0ab-461f-91ad-42a4d91d490b" />

After submitting the file for processing, the automation archives each files to processed folder like below. The processed folder is created by the automation under the given files folder if it doesn't exist

<img width="862" alt="image" src="https://github.com/user-attachments/assets/d0d2aff1-2108-45a6-9f2f-481df558a993" />

YOu can also see document requests created in data capture

<img width="556" alt="image" src="https://github.com/user-attachments/assets/3c934eca-1761-47d4-ba3e-4b794348dc8b" />

## How to deploy the accelerator

### Pre-Requisites

1. A sharepoint site and folder where folders will be uploaded
2. You need to make sure pre-requisites for Data Capture is completed as detailed in [product documentation](https://learn.microsoft.com/en-us/industry/sustainability/record-data-capture)

### Deployment steps

1. Download the managed solution for direct use and unmanaged solution for updates and extensions from the solutions folder provided in this code repository
2. Go to [PowerApps Maker Portal](https://make.powerapps.com) and select solutions, then import solution and select the solution.zip file. Select Next and proceed to connections page
<img width="1199" alt="image" src="https://github.com/user-attachments/assets/1caf35c6-280d-4cb8-bed7-b379df1f380f" />

3. Define Dataverse and SharePoint connections and Select Next

   <img width="677" alt="image" src="https://github.com/user-attachments/assets/13cbadd0-87fb-4f2c-a999-7c2b92b7e639" />

4. Define SharePoint Site (select the sharepoint site you have access to) and Site Folder path parameters (the folder under Documents library in that given SharePoint Side. For ex. Utility Bills)

   <img width="677" alt="image" src="https://github.com/user-attachments/assets/4a1f10ee-af80-43bd-ace9-d4d3bf68c030" />

6. Run the power automate named "Process Documents" 

<img width="1196" alt="image" src="https://github.com/user-attachments/assets/20f3c574-0244-4981-933e-8b525a9ae29c" />

7. Observe the document request records are created under Data capture functionality in Microsoft Sustainability Manager as below

<img width="556" alt="image" src="https://github.com/user-attachments/assets/3c934eca-1761-47d4-ba3e-4b794348dc8b" />
