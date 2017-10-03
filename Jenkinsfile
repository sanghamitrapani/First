pipeline{
  agent any
  stages{
      stage('Checkout Source code'){
      git url:'https://github.com/nogiboina/Jenkins-Project.git'
      }

      stage('Compile Stage'){
      withMaven(maven : 'M2_HOME'){
      sh 'mvn clean compile'
    }
  }
  stage('Testing Stage'){
  withMaven(maven : 'M2_HOME'){
  sh 'mvn test'
    }
  }
stage('Package Stage'){
withMaven(maven : 'M2_HOME'){
sh 'mvn install'
  }
}
stage('Package Stage'){
withMaven(maven : 'M2_HOME'){
sh 'mvn deploy'
  }
}
}
}
