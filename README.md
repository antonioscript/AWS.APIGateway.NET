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

# References
https://codewithmukesh.com/blog/amazon-api-gateway-with-dotnet/
