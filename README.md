# React-Deploy-on-Git
how to deploy react project on git hub


Deploying a React App (created using create-react-app ) to Github pages 

You can deploy any existing react app that you created - for eg - the one we created in the opening session my-contacts-app (the below steps should be done after you’ve created your react app using create-react-app and after having checked that it works on local )

Steps
1. Create an empty github repository (preferably with the same name as the project folder name -in this case my-contacts-app ) - Keep it public with no Readme.md file
2. In the terminal cd into the folder my-contacts-app
3. Install the gh-pages package as a "dev-dependency" of the app running the following commands
      a. cd my-contacts-app
      b. npm install gh-pages --save-dev
4. Open the package.json file and add the following
    a. Add a homepage property 
          "homepage": "http://{githubusername}.github.io/{reponame}",
    b. In the scripts property add 
          "scripts": {
            //...
            "predeploy": "npm run build",
            "deploy": "gh-pages -d build"
          }
5. In the terminal run the git init command
6. Add the GitHub repository as a "remote" in your local git repository
    git remote add origin https://github.com/{githubusername}/{reponame}.git
7. Generate a production build by running this command
     npm run deploy
    You are done ! - no need to add or commit or push 
8. Refresh your Github repo and check if the build files have uploaded
9. Go to ‘Settings’ ->Pages and see your github pages build link there 
10. If you make more changes to your local copy, all you need to do is
     npm run deploy and wait for 1 minute for Github to process the new build 
     
     
     
From 
https://github.com/gitname/react-gh-pages
https://create-react-app.dev/docs/deployment/#github-pages 

