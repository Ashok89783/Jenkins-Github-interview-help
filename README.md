# Jenkins-Github-interview-help
Here my self providing Questions and Answers


CICD GIT Jenkins

https://github.com/Ashok89783/ashokfirstrep

https://github.com/iam-veeramalla/Jenkins-Zero-To-Hero/blob/main/Interview_Questions.md            -------- Abhishek Veera 
https://www.youtube.com/watch?v=LAYV7x_aIC0                                                        -------- yopu tube link  Abhishek
=============================================Start ===============================================================
Q: Can you explain the CICD process in your current project ? or Can you talk about any CICD process that you have implemented ?

A: In the current project we uses tools for Jenkins to achieve CICD.
    Those are
    Mainly Jenkins is used as a orchestrator (In DevOps, an orchestrator typically refers to a tool or platform that automates and manages the deployment,         	 scaling, and orchestration of software applications and infrastructure components)
    
      For orchestration we have different tools like
    >>Maven, Sonar, AppScan, ArgoCD, and Kubernetes
For build purpose our old organisation used Java, and to make jobs automation we used python/ shell scripts.

Coming to the implementation, the entire process takes place in 8 steps

1. Code Commit: IN our organisation we used GitHub as Sourse code repository where any developer commits the code into souse code repository a jenkins pipeline is automatically triggered and as part of the first step this jenkins pipeline pulls the code from the sourse code repository and once the code was pulled and checked out the next step would be building this code,here we used 'maven'(java build tool) as part of process. (1 to 2 points)

once maven build the application the next thing that we do is we should verify code quality or we verify static code analysis or we should verify application software is secured or not.

After that we used some tool called as 'Appscan' again this used for security testing as security vulnerabilities. after this we tries to promote this Application in to Dev using Argocd and K8s. Here K8s is our platform it is our Dev environment, Here we used argocd for continuously monitor, actually argocd is a declarative continuos delivery tool. Argocd would look for K8s manifest in the git repository and when ever there is a change once the the application was built or once the new image was updated we know already Argocd will look for this new tag of the image and using help chats it would deploy 
new version of the application on the target kuberneties target clusters. 

environment 


to avoid complexity we require one example like 

We reuire a code need to explain with maven build there it consists Python code and finally there exists shell scripts --- git ripository and deploys into k8s cluster.( Need watch video at 5 min exactly) 

Here we can modify it accordingly, it mean, with out k8s we used same process to deploy in EC2 instances if organisation not migrated to k8s.
-----------------------------------------------------------------------------------------------------------------------------------------------
1. pulling this pipeline Developers commit code changes to a Git repository hosted on GitHub).
2. Jenkins Build: Jenkins is triggered to build the code using Maven. Maven builds the code and runs unit tests.
3. Code Analysis: Sonar is used to perform static code analysis to identify any code quality issues, security vulnerabilities, and bugs.
4. Security Scan: AppScan is used to perform a security scan on the application to identify any security vulnerabilities.
5. Deploy to Dev Environment: If the build and scans pass, Jenkins deploys the code to a development environment managed by Kubernetes.
6. Continuous Deployment: ArgoCD is used to manage continuous deployment. ArgoCD watches the Git repository and automatically deploys new changes to the development environment as soon as they are committed.
7. Promote to Production: When the code is ready for production, it is manually promoted using ArgoCD to the production environment.
8. Monitoring: The application is monitored for performance and availability using Kubernetes tools and other monitoring tools.

-------------------------------------------------------------------------------------------------------------------------------------------------



