# Jira Workshop: Installing and setting up Jira without Docker

## Info
Provides info and for installing a local Jira instance running for Workshop purposes.

1. [Download](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) and install the latest JDK8.
2. [Download](https://www.atlassian.com/software/jira/download-archives) the 6.3.10 version for your specific platform. For Windows and Linux: pick the installer, for Mac: pick the zip or tar.gz archive. The mentioned distributions come with an embedded Tomcat instance, when you accidentally (or on purpose) downloaded the war distribution you need to install [Tomcat](http://tomcat.apache.org/download-80.cgi) yourself and deploy the war manually.
3. Run the Jira installer.
4. Start Jira. It will run on port 8080 by default.
5. Access Jira on http://localhost:8080. The Jira configuration-screen will open. Choose: "Set it up for me", this option is enough for setting up an evaluation or demonstration environment. Choose Next, Jira will setup an in-memory database in a few minutes.
6. Almost done. Pick "Software development*" and choose Next. Create a [My Atlassian Account](https://my.atlassian.com) and generate an evaluation license for Jira. Install the license and create an administrator account.
7. Create a new Scrum-board with Board name and Project name "Workshop", Jira will generate a project key "WOR", that's OK. Select "Agile simplified workflow" and click "Create board".
8. You're ready for the Workshop! When you're done with the workshop don't forget to stop Jira. 
