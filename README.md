# 1. YouTube demo video link: 

https://youtu.be/8ngUBS84K-g 



# 2. **Reflection Questions**

## 1. What challenges did you encounter when configuring environment variables in the GitHub Actions workflow?

One challenge was understanding where to define environment variables in the GitHub Actions workflow and ensuring they were available to the build step. I also needed to match the variable names exactly with those used by the store-front application and replace localhost URLs with the deployed backend addresses. YAML indentation was another source of confusion. I checked the workflow configuration and build logs to identify and resolve these issues.



## 2. How does deploying microservices on Azure Web App Service differ from running them locally?

1) Deploying microservices on Azure Web App Service, there is no control of network ports. Every visit has to go thru https 443 port.

2) No IP address, only domain name provided by Azure Web App Services;
3) In Azure App Services, deployment is directly from GitHub code base, instead of downloading from GitHub to Linux server(in VM deployment)



## 3. Why is it important to use environment variables for configurations in a cloud environment?

Environment variables keep **configuration separate from application code**, which is important because cloud settings differ between deployments.

They allow you to:

- **Use the same code in different environments:** local development and Azure can use different service URLs and ports.
- **Keep credentials out of Git:** cloud settings or a secret manager can supply passwords and connection strings.
- **Change settings without editing code:** administrators can update connections through the cloud platform, usually followed by an application restart.
- **Automate deployments:** deployment tools can inject the appropriate settings for each environment.



# 3. Links to the three service repositories you created in lab 2:

- `order-service` https://github.com/han00163/order-service-cst8915-lab2
- `product-service`  https://github.com/han00163/product-service-cst8915-lab2
- `store-front` https://github.com/han00163/store-front-cst8915-lab2