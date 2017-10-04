pipeline {
  agent any
    tools{
    maven 'maven-3.5.0'
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
    stage('build') {
       steps {
        withEnv( ["PATH+MAVEN=${tool maven}/bin"] ) {
        sh 'mvn --version'
        sh "mvn clean install"
      }
    }
  }
}
}
