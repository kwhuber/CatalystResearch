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

# Node JS vs. Express JS
## Node JS
* an open-source and cross-platform runtime environment for executing JavaScript code outside of a browser
* Node JS is not a **framework** (Express JS is a framework) and it's not a programming language (JavaScript is the language you use with Node JS)
    * **framework:** structure that provides a foundation and reusable components for developing apps
        * includes libraries and conventions streamlining the development process by providing solutions to common problems 
        * stray from low-level details and provide higher-level **APIs** and interfaces to work with
            * **API:** an application programming interface is a set of rules that allow different software apps to communicate with each other
                * define methods and data formats that apps can use to request and exchange information
                * APIs abstract away from the complexities of underlying systems by providing a simplified way to interact with them, allowing developers to focus on using the functionality provided by the API without the need to understand the internal workings 
                * APIs follow standardized protocols such as **HTTP** for web APIs or **REST** for web services to make it easier for developers to work with different APIs
                    * **HTTP:** stands for Hypertext Transfer Protocol and is used for communication on the World Wide Web
                        * follows a client-server model where the client (web browser) sends requests to the serve for resources and the server responds with data
                        * HTTP is stateless meaning it does not retain any information about previous requests, simplifying communication but is the reason why have **cookies** or **session tokens**
                        * methods: 
                            * **GET:** requests data from a specified resource
                            * **POST:** submits data to be processed to a specified resource
                            * **PUT:** updates a specified resource with new data
                            * **DELETE:** deletes a specified resource
                            * **HEAD:** requests headers only from a specified resource without the actual data
                            * **OPTIONS:** returns the HTTP methods supported by the server for a specified resource
                    * **REST:** stands for Representational State Transfer and is an architectural style for designing networked applications
                        * in REST, everything is a **resource**
                            * **resource:** an object or piece of data that can be accessed via a unique identifier (URL)
                            * can be anything from individual data items (e.g. user profile) or collections of data (e.g. list of products)
                        * RESTful APIs simplifies client-server interactions by using standard HTTP methods to perform **CRUD** operations on resources
                            * **CRUD:** stands for Create, Read, Update, and Delete
                                * four basic functions that are used in database and web apps for managing data
                                * many web frameworks and APIs provide built-in support for CRUD operations
                                * **Create:** creating new data entries in a database (e.g. creating a new user or adding a new product to inventory)
                                * **Read:** retrieves existing data from a database (e.g. retrieving a list of all users or displaying details of a specific product)
                                * **Update:** modify existing data in a database (e.g. updating a user's profile or changing the quantity of a product in stock)
                                * **Delete:** removes existing data from a database (e.g. deleting a user account or removing a product from inventory)
        * designed to be extensible for plugins or even custom code
        * examples: 
            * web development: Express JS (for Node JS), Django (for Python)
            * font-end development: React JS, Angular 
            * mobile development: React Native, Flutter
* commonly used for building back-end services, like APIs for web applications, mobile applications, etc. 
* its scalability and extensive libraries make it attractive for building large-scale apps


## Express JS
* a framework that sits on top of Node JS's web server functionality to simplify its APIs and add helpful new features
