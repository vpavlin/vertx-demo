node ('master') {
  stage 'build'
  openshiftBuild(buildConfig: 'myapp', showBuildLogs: "true")

  stage 'deploy'
  openshiftDeploy(deploymentConfig: 'myapp')

  stage("Test") {
    input message: "Approve?", id: "approval"
  }

  stage 'deploy-prod'
  openshiftTag(srcStream: 'myapp', srcTag: 'latest', destStream: 'myapp', destTag: 'prod')
}