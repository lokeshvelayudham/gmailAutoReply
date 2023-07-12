steps:

1.creating a google cloud console for API interaction
    a. login with a google cloud account and create a project with project name and organisation name(optional)
    b. go to APIs and services enable gmail API 
    c. go to OAuth consent screen and make it exteranl user type and test mail id you would like to access
    d. go to create credentials and create OAuth clinet id, use application type as web application, and add redirected localhost urls
    e. download the client id, client secret json and save it in the root folder 

2. create index.js file 
   1. install node "npm init -y"
   2. used express framework for application "npm install express"
   3. install google api "npm i googleapis"
   4. install google auth "npm i @google-cloud/local-auth"
   5. install nodemon "npm install nodemon"
3. funcationality of gmailAutoReply:
   1. steps 1: reading the api credentaials and accessing the api by get call 
      1. Load client secrets from a local file.
      2. Authorize a client with credentials, then call the Gmail API.
   2. creating a label named Vacation 
   3. get messages that have no proper reply
   4. send reply to that message as a 64 bit encoded message
   5. Add label to a message and move it to the label folder
   6. repeat the steps 3,4,5 on random interval using random function of 45 to 120 second
