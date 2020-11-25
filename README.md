# Requirements
Make sure that you have the following installed:
- [node](https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-18-04) 
- npm 
- [MongoDB](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-ubuntu/) and start the mongodb service with `sudo service mongod start`

## Navigate to the Client Folder 
 `cd client`

## Run the folllowing command to install the dependencies 
 `npm install`

## Run the folllowing to start the app
 `npm start`

## Open a new terminal and run the same commands in the backend folder
 `cd ../backend`

 `npm install`

 `npm start`

 ### Go ahead a nd add a product (note that the price field only takes a numeric input)
 
 
 # Deloy to Google Kubernetes Engine (GKE)
 
 1. Login to GCP and create a Kubernetes Cluster on [GKE](https://console.cloud.google.com/kubernetes)
 2. Execute the following commands to deploy yolomy frontend, backend and mongo db
 
 ### Mongo DB
 
 1. Create Mongodb Deployment and Service ` kubectl create -f mongodb.yml `
 2. Confirm the service creation by executing ` kubectl get svc `
 3. Confirm the pod creation by executing `kubectl get pods`
 
 ### Yolo Client
 
 1. Create Yolomy Client Deployment and Service ` kubectl create -f yolomy-client.yml `
 2. Confirm the service creation by executing ` kubectl get svc `
 3. Confirm the pod creation by executing `kubectl get pods`
 
  ### Yolo backend
 
 1. Create Yolomy Client Deployment and Service ` kubectl create -f yolomy-backend.yml `
 2. Confirm the service creation by executing ` kubectl get svc `
 3. Confirm the pod creation by executing `kubectl get pods`
 
 To get the service IP, run below commands and get the value for ` clusterIP: `

### Yolo Client

- ` kubectl get service yolomy-client --output yaml `

### Yolo Backend

- ` kubectl get service yolomy-backend --output yaml `
 
 
