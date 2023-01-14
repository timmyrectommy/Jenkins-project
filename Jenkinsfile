pipeline {
  agent any
  stages{
    stage ('BUILD'){
      steps{
        sh 'printenv'
        sh 'docker build -t timmyrectommy/jenimg:""$BUILD_ID"" .'
      }
    }
      stage ('Publish'){
      steps{
        sh 'docker login -u $DOCKER_USERNAME -p $DOCKER_PASSWORD'
        sh 'docker push timmyrectommy/jenimg:""$BUILD_ID""'
        }
      }
        
  }
}
