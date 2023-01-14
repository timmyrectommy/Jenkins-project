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
        withDockerRegistry([credentialsId: "docker-hub", url: ""]){
          sh 'docker push timmyrectommy/jenimg:""$BUILD_ID""'
        }
        }
      }
        
  }
}
