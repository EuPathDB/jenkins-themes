Custom styling for Jenkins Simple Theme Plugin

###Setup

  - Install the [Simple Theme plugin](https://wiki.jenkins-ci.org/display/JENKINS/Simple+Theme+Plugin)
  - git clone into `$JENKINS_HOME/userContent/eupathdb`
  - In Jenkins System Configuration set Theme path to 
    `/userContent/eupathdb/<NAME>/style.css` where `<NAME>` is one of the 
    theme subdirectories.
    
####Tip

Create a job that updates the installed themes when changes are pushed to GitHub. 
Create a Free-style job with the following configuration.

  - Restrict where this project can be run: `master`
  - Use Custom Workspace: `$JENKINS_HOME/userContent`
  - Source Code Management
    - Git
      - Repository URL: `https://github.com/EuPathDB/jenkins-themes.git`
    - Additional Behaviors
      - Check out to a subdirectory: `eupathdb`
  - Build Triggers
    - Build when a change is pushed to GitHub

