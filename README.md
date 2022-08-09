### Deployment

In order to deploy the example, you need to run the following command:

```
$ serverless deploy
```

### Issue

- Inline SQS trigger causes `EventInvokeConfig` to deploy before the function which it depends on

```
The function doesn't exist. (Service: AWSLambdaInternal; Status Code: 404; Error Code: ResourceNotFoundException; Request ID: xxx; Proxy: null)
```

- When using explicit `EventConfigTrigger` instead, the deployment succeeds
- However, explicit trigger is not supported in `serverless-offline-sqs`, functionality is limited with this work-around
