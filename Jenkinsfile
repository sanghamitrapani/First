pipeline{
  agent any
  stages{
      stage('Checkout Source code'){
        steps{
        git url:'https://github.com/nogiboina/Jenkins-Project.git'
        }
      }
      stage('Compile Stage'){
        steps{
        withMaven(maven : 'M2_HOME'){
        sh 'mvn clean compile'
        }
      }
    }
      stage('Testing Stage'){
        steps{
        withMaven(maven : 'M2_HOME')
        {
        sh 'mvn test'
         }
        }
    }
      stage('Package Stage'){
        steps{
        withMaven(maven : 'M2_HOME'){
        sh 'mvn install'
        }
          }
      }
      stage('Package Stage'){
        steps{
        withMaven(maven : 'M2_HOME'){
        sh 'mvn deploy'
        }
          }
      }
}
}
