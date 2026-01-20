pipeline{
  agent any
  stages {
    stage('Build Docker Image'){
      steps {
        script {
          dockerapp = docker.build("kerenapuquecardoso/to-do-list:${env.BUILD_ID}", '-f ./Dockerfile')
        }
      }
    }

    stage('Push Docker Image'){
      steps {
        script {
          docker.withRegistry('https://registry.hub.docker.com', 'dockerhub-credentials') {
            dockerapp.push('latest')
            dockerapp.push("${env.BUILD_ID")
          }
        }
      }
    }                                                      
  }
}
