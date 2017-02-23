node ('test') {
  stage 'build'
  openshiftBuild(buildConfig: 'myapp')

  stage 'deploy'
  openshiftDeploy(deploymentConfig: 'myapp')

}