# My Repository
# My Repository
q1. You ran an Ansible playbook to install Python3 on multiple servers, but it failed on one of the servers. The error message was:
fatal: [server2]: failed! => {""msg"": ""no package matching 'python3' found available""}    
Questions:
i.     Why did this error occur?
ii.     How can you modify your playbook to handle this issue dynamically using Ansible Facts?
iii.     Write a playbook snippet that ensures Python3 gets installed correctly on any Linux distribution.

q2. Create an Ansible role that installs Python3 and deploys a custom configuration file for the application. 
Task:
i.     Create an Ansible Role named python_app_deploy with the correct directory structure.
ii.     Ensure Python3 is installed as part of the role.
iii.     Place a template file named config.yml.j2 inside the templates/ directory.
Use the template module in the role to copy config.yml.j2 to /etc/python_app/config.yml on the target machine.

Q3. a.     Write a YAML file for the below JSON Content.







{

            “name”: “Sample JSON File”

                 “hosts”: [

                                   {

                                                     “name”: “web1.abc.com”

                                                    “port”: 2222

},

                                   {

                                                     “name”: “web2.abc.com”

                                                    “port”: 22

}

 

],

“fruits”: {

                 “orange”: {

                                   “weight”: “250grm”

                 },

                 “banana”:{

                                   “weight”: “500grm”

                 }

}

}
Q4. Write an Ansible playbook to a web server on the remote host with the following conditions:       

·      Install the right package (apache2 if it is Ubuntu, httpd if is Redhat) based on the Linux distribution

·      Validate the right version is installed

·      copy the local website content to the remote host and set the permissions to 0644

·      and then start the service 

Q5. Create a simple playbook that updates all packages on a remote host as a root user.
Q6. a.     Create an Ansible inventory file and define two groups of hosts

The candidate should create an inventory file with two host groups: webservers (web1.abc.com, web2.abc.com) and dbservers (db1.abc.com, db2.abc.com). Add a variable http_port with value 8080 to the webservers group in the inventory file. 

q7.Create an Ansible playbook to create a user with a home directory and add him to the sudousers group.



jenkins-docker-kubernetes
1.     Implement a CI/CD pipeline using Jenkins multi-branch pipelines, SonarQube for code quality, Docker for containerization, GitHub webhooks and Kubernetes for deployment.
Scenario:
You are part of a DevOps team working on a Java-based microservice. The application is managed in a GitHub repository with multiple branches, each serving a different purpose. You need to create a Jenkins multi-branch pipeline that:
1.     Triggers automatically using a GitHub webhook.
2.     Builds and tests the Java application using maven.
3.     Performs SonarQube code quality analysis.
4.     Packages the application into a Docker container and pushes it to an image registry.
5.     Deploys the application to a Kubernetes cluster using YAML manifests.
6.     Implements a Git branching strategy to manage different types of deployment work.
  I.          Branching Strategy and Execution Rules
  II.           Webhook Integration
  a.     Configure a GitHub webhook that triggers Jenkins when:
    i.     A commit is pushed to any branch
    ii.     A new Pull Request is created
    III.           Building Java Code with Maven
    a.     Compile the application using Maven.
    b.     Generate .jar file as the build artifact.
    IV.           SonarQube Code Quality Analysis
      a.     Integrate SonarQube into the Jenkins pipeline.
      b.     Ensure the build fails if the SonarQube quality gate fails.
    V.           Docker Containerization and Image Push
      a.     Write a Dockerfile with the following specifications:
      i.     Base Image: openjdk:11-jre-slim
      ii.     Copies the application JAR from the build output.
      iii.     Exposes port 8080 (the application port).
      iv.     Uses ENTRYPOINT [“java”, “-jar”, “/app.jar”].
    VI.           Kubernetes Deployment

a.     Write Kubernetes manifest files that include:

 i.     deployment.yaml (Defines the app deployment and replicas).

 ii.     service.yaml (Exposes the application internally).

b.     Add Kubernetes apply command to Jenkinsfile to enable deployment. 























