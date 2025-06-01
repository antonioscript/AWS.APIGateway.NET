# AWS.APIGateway.NET
This repository demonstrates how to integrate AWS API Gateway with .NET applications. It covers key concepts such as creating and deploying REST APIs using API Gateway, integrating with Lambda or backend services and DynamoDB, configuring routes, authorizers, stages, and securing endpoints.


## Summary

- [API Gateway](#api-gateway)
- [AWS REST API vs. HTTP API](#aws-rest-api-vs-http-api)
- [Integration Types Supported by API Gateway](#integration-types-supported-by-api-gateway)
- [Creating Amazon API Gateway](#creating-amazon-api-gateway)
  - [Test Routes](#test-routes)
- [Case](#case)
  - [Test Case](#test-case)
- [Conclusion](#conclusion)
- [References](#references)



## API Gateway

![image](https://github.com/user-attachments/assets/6da87510-c62d-4cce-b8f2-488e2537d7fa)


- `www.<url-of-aws-gateway>/test` → would redirect to a Lambda named `test-lambda`
- `www.<url-of-aws-gateway>/get-students` → would redirect to a Lambda that returns a list of students
- `www.<url-of-aws-gateway>/weather?city=trivandrum` → would redirect to a public weather API endpoint which would return the weather data of Trivandrum city.


## AWS REST API vs. HTTP API

AWS supports two versions of the API Gateway Services. The initial release was for the REST API variant which includes tons of features to design, develop, and maintain your API Gateway. Later, around 2019, AWS introduced HTTP APIs which simplified the Gateway creation and deployment. Do not get confused with the naming, both of these versions are built on HTTP protocol following the REST conventions. Internally AWS names them as v1 (REST API), and v2 (HTTP API)

https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-vs-rest.html


## Integration Types Supported by API Gateway

While this repository demonstrates integration with AWS Lambda functions, it's important to note that **API Gateway supports multiple types of backend integrations**, making it a flexible tool for various architectures.

Here are the main integration types supported:

| Integration Type         | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| **Lambda Function**      | Most common integration in serverless setups. Executes a Lambda on request. |
| **HTTP/HTTPS Endpoint**  | Forwards requests to any public or private HTTP-based service (e.g. EC2, ECS, on-premises servers). |
| **AWS Service Proxy**    | Directly invokes AWS services like S3, DynamoDB, or SNS using API Gateway.  |
| **VPC Link**             | Connects to resources in a private VPC via Network Load Balancer (e.g., internal microservices, legacy apps). |
| **Mock Integration**     | Returns a mocked response without forwarding to any backend (useful for testing). |

This makes API Gateway a powerful layer for routing, securing, and managing APIs across both **serverless** and **traditional** architectures.



## Creating Amazon API Gateway

</br>

![image](https://github.com/user-attachments/assets/56479bb4-8bc9-469f-8c3e-5e3c44b482c2)

-----

![image](https://github.com/user-attachments/assets/bca6561f-71f5-49b6-99f0-c1547f87cd3a)

----

![image](https://github.com/user-attachments/assets/e07a5a9b-de1e-4132-b60b-020d3bd30740)

----

![image](https://github.com/user-attachments/assets/93adeecc-7e1b-4b85-b580-aae86bd1475b)


-----

</br>

</br>

</br>


### Test Routes

![image](https://github.com/user-attachments/assets/cb7d6479-9fae-48f0-945b-407e30807ed8)

------

</br>

**Or**

</br>

![image](https://github.com/user-attachments/assets/6694dfff-7b62-48dd-bfee-5a8b8bd1179e)

----
![image](https://github.com/user-attachments/assets/359ee093-8c86-4f95-a492-b8e8f3dedf1a)


## Case

_> We now have three more created lambdas functions_

</br>

</br>

![image](https://github.com/user-attachments/assets/1c2c0c15-034e-4438-8059-f131d5ce533d)

-----

</br>
</br>

_> Let’s create a new API Gateway for them_

-----

![image](https://github.com/user-attachments/assets/e6aef2ed-21d9-43fd-bc9a-20fb3f214bb0)


-----

![image](https://github.com/user-attachments/assets/936c520d-400b-4ce7-b5f4-b3c8dd53d7f9)

-----

![image](https://github.com/user-attachments/assets/2c62550a-d0a6-4830-ab61-bf7c61300622)

-----

![image](https://github.com/user-attachments/assets/66ec866e-9693-4134-a142-754060de34d9)


------

</br>
</br>
</br>


### Test Case

![image](https://github.com/user-attachments/assets/fa721899-3ca6-4234-89d9-571d748abda4)

------

![image](https://github.com/user-attachments/assets/bb3e4ab5-166f-4a73-bac2-9335fe07d80d)

-----

![image](https://github.com/user-attachments/assets/bc1450eb-6e15-4a54-930d-6e55ee6eadac)

------

## Conclusion

In this example, we demonstrated how API Gateway can be used to centralize access to multiple Lambda functions. Instead of creating separate public endpoints for each Lambda — which would require multiple URLs, configurations, and individual integrations — we used a single API Gateway to manage everything.

With this approach, we achieved:

- **Grouping multiple Lambda functions** (such as `/test`, `/get-students`, `/weather`) under a single API structure  
- Reduced complexity in exposure and security, since all requests go through a single entry point  
- Centralized control for authentication, monitoring, and logging  
- Easier route organization and versioning

In short, API Gateway serves as a **smart and unified entry point** for multiple services — which is essential in modern, especially serverless, architectures.



# References
https://codewithmukesh.com/blog/amazon-api-gateway-with-dotnet/
