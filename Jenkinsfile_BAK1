node {
     cleanWs()
     checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'git@github.com:nogiboina/Jenkins-Project.git']]])
     sh 'mvn clean compile install'
     archiveArtifacts '**/*.jar'
    
}