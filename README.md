# Build-a-Node-RED-starter-dashboard-application-in-IBM-Cloud

## Step 1: Create IBM Cloud account

Signup/Sign-in on IBM Cloud account: https://ibm.biz/node-red-workshop

## Step 2: create the Node-RED Starter application.

Open the catalog and search for node-red. Click on the Node-RED App tile

<img width="589" alt="1" src="https://user-images.githubusercontent.com/16270682/110790153-1d15d580-828a-11eb-9ab0-d82c10e9a9b2.PNG">

On the Create tab, a randomly generated App name will be suggested. Either accept that default name or provide a unique name for your application. This will become part of the application URL.

#### Note: If the name is not unique, you will see an error message and you must enter a different name before you can continue.

<img width="515" alt="2" src="https://user-images.githubusercontent.com/16270682/110790165-21da8980-828a-11eb-9b92-cb7e6b011fff.PNG">

Click the Create button to continue. This will create your application, but it is not yet deployed to IBM Cloud.

<img width="570" alt="3" src="https://user-images.githubusercontent.com/16270682/110790309-54848200-828a-11eb-9207-248745b82000.PNG">

## Step 3. Enable the Continuous Delivery feature

click the Deploy your app button to enable the Continuous Delivery feature for your application.

<img width="908" alt="4" src="https://user-images.githubusercontent.com/16270682/110790322-58b09f80-828a-11eb-8040-567c5befcc4e.PNG">

Select Cloud Foundry from deployment target option 

<img width="635" alt="5" src="https://user-images.githubusercontent.com/16270682/110790351-61a17100-828a-11eb-8d01-111816ddb65e.PNG">

You will need to create an IBM Cloud API key to allow the deployment process to access your resources. Click the New button to create the key. A message dialog will appear. You can accept the default values and confirm to close the dialog.Also Increase the Memory allocation per instance slider to at least 128MB. If you do not increase the memory allocation, your Node-RED application might not have sufficient memory to run successfully.

<img width="672" alt="6" src="https://user-images.githubusercontent.com/16270682/110790371-65cd8e80-828a-11eb-8e0b-7b4d0689e685.PNG">

Configure the DevOps toolchain by selecting the region it should be created in. Again, try to match the region you selected previously. Click Create. 

<img width="450" alt="7" src="https://user-images.githubusercontent.com/16270682/110790394-6b2ad900-828a-11eb-91be-d7d904b751f9.PNG">

Refresh the page, the Deployment Automation section will show details of your newly created Delivery Pipeline. The Status field of the pipeline will eventually show In progress. That means your application is being built and deployed.

<img width="855" alt="8" src="https://user-images.githubusercontent.com/16270682/110790414-71b95080-828a-11eb-8d29-dfa60a9dbca8.PNG">

Click the Status field to see the full status of the Delivery Pipeline. The Deploy stage will take a few minutes to complete. You can click on the View logs and history link to check its progress. Eventually the Deploy stage will go green to show it has passed. This means your Node-RED Starter application is now running.

<img width="535" alt="9" src="https://user-images.githubusercontent.com/16270682/110790440-77169b00-828a-11eb-866f-0ba29115ac29.PNG">

## Step 4: Open and Configure your Node-RED application

on the application details page click on the App URL to open up your Node-RED application in a new browser tab.

<img width="562" alt="10" src="https://user-images.githubusercontent.com/16270682/110793205-c8745980-828d-11eb-9494-ff45b6a5288d.PNG">

On the initial screen, click Next to continue. Secure your Node-RED editor by providing a username and password. If you need to change these at any point, you can either edit the values in the Cloudant database, or override them using environment variables. The documentation on nodered.org describes how to do this. Click Next to continue. Click Finish to proceed. 

<img width="1256" alt="11a" src="https://user-images.githubusercontent.com/16270682/110793734-67995100-828e-11eb-9c51-e4088c9251fa.png">

Node-RED will save your changes and then load the main application. From here you can click the Go to your Node-RED flow editor button to open the editor.

<img width="1191" alt="11" src="https://user-images.githubusercontent.com/16270682/110793739-69631480-828e-11eb-8cb4-04098f8ea774.png">

The Node-RED editor opens showing the default flow.

## Step 5: Add Dashboard nodes to your Node-RED palette

On your application’s details page, click Source url

<img width="650" alt="12" src="https://user-images.githubusercontent.com/16270682/110795286-1ab67a00-8290-11eb-9577-e18086fb47f9.PNG">

This will take you to a git repository where you can edit the application source code from your browser. Scroll down the list of files and click on package.json. This file lists the module dependencies of your application.

<img width="771" alt="13" src="https://user-images.githubusercontent.com/16270682/110795289-1b4f1080-8290-11eb-8b46-c38f53e4261a.PNG">

Click the edit button and Add following in dependecies section 

     "node-red-dashboard": "2.x",
 
 <img width="660" alt="14" src="https://user-images.githubusercontent.com/16270682/110795280-18ecb680-8290-11eb-9abb-60992bcdefc4.PNG">
 
 ##### Note: Do not forget the comma (,) at the end of the line to separate it from the next entry.
 
  click Commit changes

