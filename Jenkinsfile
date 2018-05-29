pipeline {
  agent any
    tools{
    maven 'maven-3.5.0'
    jdk 'JDK1.7'
     }
// using the Timestamper plugin we can add timestamps to the console log
options {
    timestamps()
}
stages {
  stage ('Initialize') {
    steps {
      sh '''
        echo "PATH = ${PATH}"
        echo "M2_HOME = ${M2_HOME}"
         '''
      }
    }
stage ('Testing Checkout') {
steps{
sh 'echo "Before taking the Checkout the code from GITHUB"'
}
}
stage ('Build') {
  steps {
    sh 'mvn -Dmaven.test.failure.ignore=true install'
    }
    post {
      success {
        junit 'target/surefire-reports/**/*.xml'
            }
         }
    }
  }
}
