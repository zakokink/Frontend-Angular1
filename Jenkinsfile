pipeline {
  agent any
  environment {
        IMAGE_REPO_NAME="frontend_angular"
        IMAGE_TAG="v1"
        AWS_DEFAULT_REGION="eu-central-1"
        AWS_ACCOUNT_ID="992382586240"
        REPOSITORY_URI="992382586240.dkr.ecr.eu-west-2.amazonaws.com/frontend_angular"
    
        }
  stages {
    stage("BUILD DOCKER IMAGE") {
      steps {
        script {
          dockerImageBuild = docker.build "${IMAGE_REPO_NAME}:${IMAGE_TAG}"
        }
      }
    }
     
    }
  }
