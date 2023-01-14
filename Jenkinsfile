pipeline {
  agent any
  stages{
    stage ('BUILD'){
      steps{
        sh 'printenv'
        sh 'docker build -t Timmyrectommy/jenimg:""$BUILD_ID"" .'
      }
    }
      stage ('Publish'){
      steps{
        withDockerRegistry([credentialsId: "docker-hub", url: ""]){
          sh 'docker push Timmyrectommy/jenimg:""$BUILD_ID""'
        }
      }
        
      }
  }
}
