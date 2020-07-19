# GCP AppEngine

A package to create and get information about Google AppEngine Application. 

## How to use it?

Package reuired project owner permission to create the AppEngine Application. 


```
import Gcp from "@myjunior/gcp-appengine";
const keyFile = "service-account-key.json"
const gcpProjectId = "project-xyz";
const gcp = new Gcp(keyFile);

// create AppEngine Application
gcp.createInstance(gcpProjectId).then((resp)=>{
  console.log(resp);
}).catch(err=>{
  console.log(err);
});

// Get AppEngine Application
gcp.getInstance(gcpProjectId).then((resp)=>{
  console.log(resp);
}).catch(err=>{
  console.log(err);
});


```


## Develop 

* Create a service account with `owner` permission 
* export Google Cloud Auth Environment variable `export GOOGLE_APPLICATION_CREDENTIALS="key.json"`

## NPM publish 

* create a access token with read+publish permission
* set access token as environment variable `export NPM_TOKEN="000-000-0000-00000"`
* run `npm run push` command 

