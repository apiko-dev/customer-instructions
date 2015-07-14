####To clone repository you need to follow this steps:

0) Open terminal and go to directory where repo folder should be cloned to like:
```
cd ~
#repo will be cloned into your home directory
#by default terminal will be opened there
```
1) ensure you have GIT:
```
git --version
```
Output (if you already have GIT) will be something like: `git version 2.3.2 (Apple Git-55)`

2) if you don't then install it:

http://git-scm.com/download/mac

Download and install GIT package. Then goto step #0.

3) Finally you can clone repo with command:
```
git clone https://repository.url
```
While executing this command you need to enter login and password from your bitbucket account.

Now files are ready for editing.

####If you would like to run application locally (in oder to check everything) you need follow this steps:

1) Install meteor:
```
sudo curl https://install.meteor.com/ | sh
```
2) Go into folder with application repository. In case if you cloned repo into home directory (`cd ~`) you should go into:
  `cd ~/application-name`

3) Run Meteor app with command (```sudo``` may be required):
```
meteor
```
In case there is a message 'Can't listen on port 3000. Perhaps another Meteor is running?' - run meteor on the another port (```sudo``` may be required):
```
meteor -p 2000
```
If app was started successfully you will see next output:
```
=> Started proxy.
=> Started MongoDB.
=> Started your app.
=> App running at: http://localhost:3000/
```

4) Now you can open application in browser by navigating to URL:
`http://localhost:3000/`.

__Note:__ After starting app you __don't__ need to restart it each time you make changes in application's files. Meteor will restart app automatically after file changes detecting. 

5) To stop application just press `Ctrl+C` in terminal window where application was started.


####In order to upload your changes to repository (make a commit) you need follow this steps in "Terminal":

0) Ensure you are in repository's root directory (in this example: `~/application-name`).

1) Add all changed files to next commit by command:
```
git add --all
```

2) Commit files:
```
git commit -m "Short description of changes you have made should be here"
```

3) Upload files to repository (make push):
```
git push origin master
```

Again, you probably need to enter user name and password for Bitbucket.
