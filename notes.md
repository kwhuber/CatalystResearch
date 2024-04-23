# Continuous Integration and Continuous Delivery/Deployment (CI/CD)
* Aims to streamline and accelerate the software development life cycle. 
* CI/CD helps organizations avoid bugs and code failure while maintaining a continuous cycle of software development and updates. 

## CI 
* facilitates more frequent merging of code changes back to a shared branch
* the goal is to have as multiple developers working simultaneously on different features of the same app
* once a developer's changes to an app are merged, those changes are validated by running different levels of automated testing, like unit and integration tests to ensure the changes haven't broken anything
* it's easier to fix bugs more often than all at the end where everything could be potentially broken

## CD
* stands for continuous delivery and/or continuous development
* **continuous delivery:** automates the release of validated code to a repo following the automation of builds and unit/integration testing in CI
    * continuous delivery usually means a developer's changes to an app are automatically bug tested and uploaded to a repo, where they can then be deployed to a live production environment by the operations team
    * continuous delivery's ultimate purpose is to have a codebase that is always ready for deployment to a production environment
* **continuous deployment:** an extension of continuous delivery and refer to automating the release of a developer's changes from the repo to production, where it's usable by customers

* Taken all together, CI/CD make the deployment process less risky, making it easier to release changes to apps in small pieces rather than all at once

# DevOps
* DevOps is a set of practices/tools that aim to improve collaboration between software development (Dev) and IT operations (Ops) teams
* **automation:** DevOps automates repetitive tasks like building, testing, and deployment
* **CI/CD:** DevOps emphasizes the adoption of CI/CD practices to automate integrating code changes, running tests, and deploying software to production
* **Infrastructure as Code:** practice of managing infrastructure like servers, networks, or databases through code and automation tools
    * for example, AWS CloudFormation is a tool used for implementing IaC and it uses JOLSON and YAML templates
    * Terraform is another example which is an open source tool used for managing infrastructure resources across multiple cloud providers and on-premise environments

