pipeline {
  agent any
    tools{
    maven 'maven-3.5.0'
    jdk 'jdk1.7.0_75'
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
stage ('Checkout Code base from GIT') {
steps{
		sh 'echo "Before taking the Checkout the code from GITHUB"'
	}
}
stage ('Build the code using Maven') {
  steps {
    sh 'mvn clean compile install'
    }
    post {
      success {
         archiveArtifacts '**/*.jar'
            }
         }
    }
  }
}
