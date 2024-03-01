pipeline {
  agent any
  environment {
    registry = ''
    registryCredential = 'dockerhubcredentials'
  }
  stages {
    stage("BUILD DOCKER IMAGE") {
      steps {
        script {
          dockerImageBuild = docker.build registry + ":latest"
        }
      }
    }
     stage("DEPLOY DOCKER") {
       steps {
          script {
            docker.withRegistry('', registryCredential) {
              dockerImageBuild.push()
            }
         }
      }
   }
    stage("DEPLOY & ACTIVATE") {
      steps {
        echo 'Deploy on ECS'
      }
    }
  }
}
