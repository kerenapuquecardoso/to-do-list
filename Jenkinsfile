pipeline{
  agent any
  stages {
    stage('Build Docker Image'){
      steps {
        sh 'dokcer build -t to-do-list .'
      }
    }
  }
}
