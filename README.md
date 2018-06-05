# React-Cloud-Photos
A simple clone of Google Cloud Photos built with react for the web

## Setting up firebase

1) Go to firebase.com
2) Go to the console and start a new project
3) Go to authentication from the menu on the left and enable email under sign up methods
  
  <img width="1439" alt="firebase auth" src="https://user-images.githubusercontent.com/33552991/41003230-48f2bfee-6927-11e8-8ed8-3d2ae85318c2.png">
  
4) Next go to databse right below the authentication option, create a real time database
5) Under the rules tab enter this in
  <code>
    {
      "rules": {
        "users": {
          "$uid":{
            ".read" : "$uid === auth.uid",
            ".write": "$uid === auth.uid"
          }
        }
      }
    }
  </code>

6) Next go to databse right below the Storage option and click on get started

## Running the project

Install Node: https://nodejs.org/en/

Open a terminal in the directory run these two commands

  <code>
    npm install
  </code>
  
  <code>
    npm start
  </code>
