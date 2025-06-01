# AWS.APIGateway.NET
This repository demonstrates how to integrate AWS API Gateway with .NET applications. It covers key concepts such as creating and deploying REST APIs using API Gateway, integrating with Lambda or backend services and DynamoDB, configuring routes, authorizers, stages, and securing endpoints.

## API Gateway

![image](https://github.com/user-attachments/assets/6da87510-c62d-4cce-b8f2-488e2537d7fa)


- `www.<url-of-aws-gateway>/test` → would redirect to a Lambda named `test-lambda`
- `www.<url-of-aws-gateway>/get-students` → would redirect to a Lambda that returns a list of students
- `www.<url-of-aws-gateway>/weather?city=trivandrum` → would redirect to a public weather API endpoint which would return the weather data of Trivandrum city.


## AWS REST API vs. HTTP API

AWS supports two versions of the API Gateway Services. The initial release was for the REST API variant which includes tons of features to design, develop, and maintain your API Gateway. Later, around 2019, AWS introduced HTTP APIs which simplified the Gateway creation and deployment. Do not get confused with the naming, both of these versions are built on HTTP protocol following the REST conventions. Internally AWS names them as v1 (REST API), and v2 (HTTP API)

https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-vs-rest.html

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


# References
https://codewithmukesh.com/blog/amazon-api-gateway-with-dotnet/
