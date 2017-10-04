pipeline {
  agent { any 'maven:3.5.0' }
  stages {
    stage('build') {
      def maven = 'maven-3.5.0'
      steps {
        withEnv( ["PATH+MAVEN=${tool maven}/bin"] ) {
        sh 'mvn --version'
        sh "mvn clean install"
      }
    }
  }
}
}
