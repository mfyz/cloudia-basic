## Basic Lambda function using Claudia

## To Deploy

First deployment:

```
claudia create --region us-east-1 --handler lambda.handler
```

to make repeat deployments:

```
claudia update
```

## To Test from cli

```
claudia test-lambda
```

with event data:

```
claudia test-lambda --event event-file.json
```

or

```
echo '{"name": "Fatih"}' | claudia test-lambda --event /dev/stdin
```

## Logs

To check the logs after invoking:

```
aws logs filter-log-events --log-group-name /aws/lambda/cloudia-basic
```