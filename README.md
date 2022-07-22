# aws-typescript-sampler

This template demonstrates how to make a simple HTTP API with Node.js and Typescript running on AWS Lambda and API Gateway using the Serverless Framework.

It uses the serverless-typescript plugin which works out of the box!

## Setup

### Create serverless project

+	Parent folder type:  ``` serverless ``` (then follow prompts)
+	CD into project folder
+	Type: ```npm init -y```
+	Create scripts in package.json to test
```json
  "scripts": {
    "local-hello": "serverless invoke local -f hello",
    "local-api": "serverless offline start --printOutput",
    "deploy": "serverless deploy --verbose",
    "remote-hello": "serverless invoke -f hello",
    "remove": "serverless remove"
  },
```
### Install dev packages
```bash
yarn add --dev serverless-plugin-typescript typescript
# or
npm install -D serverless-plugin-typescript typescript

npm i -D serverless-offline
```

### Add to serverless.yml
```yml
plugins:
  - serverless-plugin-typescript
  - serverless-offline
```
## Reference commands:
```
serverless deploy    Deploy changes
serverless info      View deployed endpoints and resources
serverless invoke    Invoke deployed functions
serverless --help    Discover more commands
```

