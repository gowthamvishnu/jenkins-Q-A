# jenkins-Q-A
                                                        Jenkins interview Q&A
 1. what is Jenkins?
 * Jenkins is a very popular tool used for continues integration. 
 * using  Jenkins one can pull the latest code from git repository and produce build which can finally be deployed to test (or) production server.
 * It can be at set to trigger a new build automatically as soon as there is a change in the git repository (or) manually  on click of button. 
 
2.Explain CI?
*This is the stage where the code functionality is integrated with the existing code. since there is continuous  development of software.
*The updated code needs to be integrated continuously  as well as smoothly with  the systems to reflect changes to the end user.
*The changed code should also ensure that there are no errors in the runtime environment. allowing 
us to test the changes and check how it reacts with other changes.
EX: Jenkins

3.Explain CD?
* It is the stage where the code is deployed to the production environment.
* Here we ensure that the code is correctly deployed on all the servers.
* If any addition of new feature ( or) functionality is introduced then one should be ready to welcome greater website traffic.
*So it is also the responsibility of the system admin to scale up the server to host more users.
*Since new code is continuously deployed on continuous  basis. configuration management tools play an important role for executing task quickly and frequently.

4.Expalin Jenkins pipeline?
* it means pipeline as a code. that means usually we create a job manually by choosing  New item in our jenkins  console.
* And we will provide steps like cloning the repository, building the code and deploying  into the target environment these are the steps we provide in the jenkins job itself.
* Rather than providing them as a jenkins job we can create or convert those into a jenkins file and and will pass that jenkins file to the jenkins job.
* so it reads our jenkins file and act according to the steps what we have given in our jenkins file. so whenever  
we talk about jenkins  pipeline we  need a file that file is called jenkins file.
 
5.explain continuous delivery?

6.what is jenkins file?
* The file which contains the jenkins pipeline as a code. 

7.EXplain about scripted and declarative pipeline?
* There are two ways to create a jenkins pipeline.
 *scripted pipeline   
 * Declarative pipeline
 *scripted pipeline: when ever jenkins jobs were launches they used scripted pipeline.
 * But to write scripted pipeline we you should have knowledge on groovy script.
             * syntax: node {
                                  stage( ) }
                                           //groovy script
                                }
	        }


 *Declarative pipeline: They recently introduce declarative pipeline. it is easy to write jenkins pipeline         comparative to scripted pipeline.
    *syntax
 pipeline {
    agent any
    }
    stages {
        stage('cloning repo') {
            steps {
                git 'https://github.com/gowthamvishnu/spring-petclinic.git'
            }
        }
Agent:  where to build
stages: where work happens.
stage: what to do

8.what are the jenkins upstream and downstream  jobs? how do u configure it?

9.how do u take jenkins backup?

10.expalin about different types of jobs in jenkins?

11.Difference between freestyle and pipeline and maven projects?

12.how do you start and  restart jenkins?
A) go to the location where jenkins is install and run this command  java -jar jenkins .war

13.explain build parameters in jenkins?

14.jenkins runs on which port and how do u change it?
A) jenkins runs on 8080 port.
   Go to the directory where you installed Jenkins (by default, it's under Program Files/Jenkins)
   Open the Jenkins. xml configuration file.
   You can find --httpPort=8080 and replace the 8080 with the new port number.
   Restart your Jenkins server.
15.explain about build types you  are using in your  organization?

16.explain master slave architecture or master slave configuration?

17)explain about build peridically,poll scm?
   poll scm:
  * "Poll SCM" polls the SCM periodically for checking if any changes/ new commits were made and shall build the project if any new commits were pushed since the last build. 
   Build periodically:
  *  whereas the "build" shall build the project periodically irrespective to whether or not any changes were made.

18)What are the system requirements to install Jenkins?
A)The minimum configuration required is 
256MB of RAM
1 GB of drive space
Java
Web browser

19) How do you install Jenkins?
A) To install Jenkins, make sure the following are installed –
Java (version 8)
Apache Tomcat (version 9)
Download the Jenkins war file and deploy it using Tomcat. You can choose to install the plugins suggested by Jenkins during the installation itself. Once the installation is done, you will be able to see the Jenkins dashboard.

20)Give some important plugins in Jenkins.
A)Here you go –
Maven 2
Gits
Amazon EC2
Join
Copy artifact
Green Balls
HTML Publisher

21) What is Groovy?
A)Groovy from Apache is a language for Java platform. It is the native scripting language for Jenkins. Groovy-based plugins enhance Jenkins with great interfaces and build reports that are dynamic and consistent.

22)How to change jenkins default port?
a)In windows:
  go to the location where jenkins is installed..if it is windows machine from command line use  
  cmd: java -jar jenkins.war --httpport=9090
  In case you want to change the default jenkins port on Linux,
  You can go to /etc/default/jenkins  
  Add --httpPort=9999 or whatever port to JENKINS_ARGS.
  Then you should restart Jenkins with sudo service jenkins restart.

