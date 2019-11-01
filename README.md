## Getting Started

Install serverless framework.

https://serverless.com/framework/docs/providers/aws/guide/installation/


## Set your User Pool

Edit `serverless.yml` and set your user pool Arn. Replace xxxxxxxxxxxxxxxxx to user pool Arn.

```
functions:
  hello:
    handler: handler.hello
    events:
      - http:
          path: hello
          method: get
          cors: true
          integration: lambda
          authorizer:
            name: authorizer
            arn: xxxxxxxxxxxxxxxxx
```

## Deploy

```
serverless deply
```