pipeline {
  agent none
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/nareshjavvaji100/mango.git', branch: 'master', credentialsId: 'nareshjavvvaji100')
      }
    }
    stage('build') {
      steps {
        echo 'build'
        sh 'mvn clean -Dmaven.test.failure.ignore= true install'
      }
    }
  }
  environment {
    dev = 'test'
  }
}