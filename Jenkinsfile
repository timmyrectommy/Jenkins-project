pipeline {
  agent any
  stages{
    stage ('BUILD'){
      stpes{
        sh 'printenv'
        sh 'docker build -t timmyrectommy/jenimg:""$BUILD_ID"" .'
      }
    }
      stage ('Publish'){
      stpes{
        withDockerRegistry([credentialsId: "docker-hub", url: ""]){
          sh 'docker push timmyrectommy/jenimg:""$BUILD_ID""'
        }
      }
        
      }
  }
}
