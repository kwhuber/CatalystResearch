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

# Keycloak
* Keycloak is an open source Identity and Access Management (IAM) solution designed to secure applications and services, providing a set of features to handle user authentication and authorization
* **Identity Management:** deals with identifying and managing users; things like user registration, user profile management, and managing credentials
* **Access Management:** who can access what within an application, typically through roles and permissions 
* **Authentication:** process of verifying who a user is; Keyclock supports various authentication methods like username/password, social logins (Google, Facebook), and single sign-on (SSO)
* **Keycloak Components:** 
    * **Realms:** a realm is a space within Keycloak where you manage a set of **users**, credentials, **roles**, and **groups**
        * realms are isolated from one another, meaning users in one realm cannot see or interact with users in another realm
        * **Users:** individuals who have accounts in a realm
        * **Roles:** a way to assign permissions to users
            * Keycloak supports realm roles and **client** roles
                * **Client:** a client in Keycloak represents an application or service; clients request authentication from Keycloak
                    * e.g. web applicationns, mobile applications, RESTful web services
        * **Groups:** collections of users that can be managed together
    * **Identity Providers (IdPs):** external systems that can authenticate users
        * e.g. social networks (Google, Facebook) and enterprise systems (**LDAP**, **Active Directory (AD)**)
            * **LDAP:** an interface for communicating with directory services such as **AD**
            * **AD:** provides a database and services for IAM
* How Keycloak works
    * install Keycloak on a server
    * create a realm for your application
    * define clients representing your applications
    * set up identity providers if you want to use external authenticaion
    * configure roles and groups as needed
    * integrate your applications with Keycloak; this typically involves configuring the application to use Keycloak for authentication and authorization 
    * use the Keycloak admin console to manage users, monitor login activity, etc.

# OAuth2 Proxy 
* OAuth2 Proxy is an open-source **reverse proxy** and authentication service
* OAuth2 Proxy is designed to secure web applications by requiring users to authenticate through an **OAuth 2.0** or **OpenID Connect (OIDC)** provider before accessing the application; it integrates with various identity providers (IdPs) like Google, Github, Azure AD, and more; once users authenticate successfully, OAuth2 Proxy forwards the authenticated requests to your application
    * **Reverse Proxy:** a reverse proxy sits in front of your web server, receiving client requests and forwarding them to the appropriate backend service; OAuth2 Proxy adds an authentication layer to this process
    * **OAuth 2.0:** an authorization framework that allows third-party services to exchange credentials and authorize user access
    * **OIDC:** an identity layer on top of OAuth 2.0 that provides authentication and user info
* How it works: 
    * user requests access to a protected resource (e.g. web application)
    * OAuth2 Proxy intercepts the request and checks for an existing authenticated session
    * if no session exits, OAuth2 Proxy redirects the user to the identity provider's login page
    * the user authenticates with the IdPs
    * the IdPs redirects the user back to OAuth2 Proxy with an authorization code
    * OAuth2 Proxy exchanges the authorization code for an access token and possibly a refresh token 
    * OAuth2 Proxy creates a session for the user and sets a cookies to manage the session 
    * the user is redirected to the original resource request, now with an authenticated session
* One of the IdPs that OAuth2 Proxy supports is Keycloak and others include Google, Github, Azure AD, etc.

# Nginx
* pronounced "engine-x"
* open-source software originally created as a **web server** designed for maximum performance and stability...over time it has evolved to include reverse proxying, load balancing, caching, and more 
    * **Web Server:** Nginx can serve static files (HTML, CSS, and JavaScript) directly to clients; can handle large number of requests simultaneously    
        * as a web server Nginx is responsible for handling HTTP requests from clients (such as web browsers) and serving web content (HTML pages, CSS, JavaScript files, and images)
    * **Reverse Proxy:** as a reverse proxy, Nginx sits between clients and backend servers, forwarding client requests to the appropriate backend service and returning the server's response to the client
        * this is useful for load balancing, caching, and securing backend services
    * **Load Balancer:** Nginx can distribute incoming traffic across multiple backend servers to balance the load and improve performance
        * such algorithms include round-robin, least connections, and IP hash
    * **Caching:** Nginx can cache responses from backend servers to reduce the load and improve the speed of serving repeated requests; this is useful for dynamic content that doesn't change often
* Nginx will forward requests through OAuth2 Proxy
