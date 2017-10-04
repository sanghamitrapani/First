pipeline {
  agent any
    tools{
    maven 'maven-3.5.0'
    jdk 'JDK1.7'
     }
    stages {
    stage ('Initialize') {
            steps {
                input message: "Check the PATH and M2_HOME variables"
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            }
    }
    stage ('Build') {
            steps {
                  input message: "Starting the build part using maven tools"
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
