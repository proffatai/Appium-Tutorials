## Android studio setup

Start android studio and ennsure you have set these: 

export PATH=$PATH:/usr/local/git/bin:/usr/local/bin:
export ANDROID_HOME=/users/mac/library/android/sdk
export PATH=$PATH:$ANDROID_HOME/platform-tools
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/emulator
export PATH=$PATH:$ANDROID_HOME/tools/bin

in your `cat ~/.zshrc` file.

Go to terminal and run the following commands to be sure that everything is fine

`adb devices` , `adb` , `emulator` , hopefully there wont be any error, then we are good to go

Launch your emulator, and take note of the name of the emulator when you were creating it because you will need it when setting desired capabilities.

## Node and Appium setup
 Stay on node 14.17.3
 
 Install Appium server (the 2.0 version) using the command, `npm install -g appium@next` 
 
 Install some basic drivers: `appium driver install uiautomator2` and `appium driver install xcuitest`
 NB: Use `appium driver list` command to verify that the drivers have been installed.
 
 To run the appium server, just type: `appium`
 NB: The server is started on port: 4723
 
## JAVA setup
 stay on java 11 and browse how to set java to path so that you can run the command `java -version` on your CLI
 
## Project Setup

1. Create a java project

2. Right click on the project name and click configure, then click convert to Maven , Set the group id and artifart id
NB: Group ID can be seen as the title of the project and the artifart ID is the 

3.  Right click on the project name again and now click Maven, click update project, check the force update option and click OK

4. Go to the src folder and clear all the files in it. Then proceed to create a package inside the src folder
NB: How to create a package: Right click on the src folder, click New, click package and give it name 
NB: Right click on the package, click New and click Class to create a Java class

5. Go to your pom.xml and paste the testNG  and java-client dependency from maven repository into a dependencies tag(create it)
NB: Create this dependencies tag just beneath the version tag

## Pushing code to GitHub from Eclipse IDE
Create a new repo on Github first
Now go to eclipse IDE and right click on your project name, click Team, click Shared Project, Click on the create button and Click  on finish, then click finish again
NB: This action is synonymous to git init because the momemt we clicked the finish button the second time, a local git file is created

Right click on the project name again, and click on Teams then click commit
Now, drag the files from the unstaged changes area into the staged changes area and enter a commit message and click on commit and push button
 
Go to github and copy the url to the newly created repo and paste it in the url field of the moodal that poped up.Click Next 2x and enter your github credentials to finalize the push
