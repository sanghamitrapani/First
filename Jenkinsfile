pipeline {
  agent { any 'maven:3.5.0' }
  stages {
    stage('build') {
      steps {
        sh 'mvn --version'
        sh 'mvn install'
      }
    }
  }
}
