pipeline {
  agent { any }
    tool{
    def maven = 'maven-3.5.0'
     }
    stages {
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
