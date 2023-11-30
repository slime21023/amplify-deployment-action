# Amplify Deployment Action

The `amplify-deployment-action` GitHub action creates a deployment into an existing Amplify aplication.
As this use the AWS SDK, credentials should be set beforehand on env variables. (inprised by [luisgreen/amplify_deployment](https://github.com/luisgreen/amplify_deployment/))

## Usage

```yml
- uses: slime21023/amplify-deployment-action@main
  with:
    # Amplify Application ID
    # required: true
    appId: ''

    # Amplify Application branch to deploy
    # required: true
    branchName: ''

    
    # Path where the artifact is located to be deployed
    # required: true
    artifactPath:

    # Region of the Amplify Application
    # required: true
    region:
```

## Sample

```yml
- uses: slime21023/amplify-deployment-action@main
  with:
    appId: 'asd8adsjasd9'
    branchName: 'prod'
    artifactPath: 'dist/release.zip'
    region: 'ap-northeast-1'
```