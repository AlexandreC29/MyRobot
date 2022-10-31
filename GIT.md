# MyRobot : git configurations

**1. Git initialization and configuration**

- git init
- git config --global user.email <your email adresse>
- git config --global user.name <your user name>

**2. Add origin from the repository**
- git remote add origin https://github.com/AlexandreC29/MyRobot.git
  
**3. Download the repository**
- git pull https://github.com/AlexandreC29/MyRobot.git

**4. Cration of a token using github**
- On the top right, click on your logo and go to Settings => Developer settings => Personnal acces token => Token (classic) => generate new token => generate new token (classic),
- Choose a name or a description for the token,
- Choose 1 year for the validity of the token 
- Select the following boxes : admin:org, delete_repo, project, repo, write:package
- Click on "generate token" and copy your personal access token : you won’t be able to see it again.
  
**5. Make change on the repository** 
- git add .
- git commit -m "message"
- git push https://github.com/AlexandreC29/MyRobot.git

You must indicate your user name and your password. The password is your personnal acces token
