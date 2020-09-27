
pipeline{
    agent {label 'java'}
    environment{
       PATH = "/usr/share/maven/bin:$PATH"
    }
    
    stage('Git Checkout') {
            steps{
               
                checkout([$class: 'GitSCM',
                    branches: [[name: '*/master']],
                    doGenerateSubmoduleConfigurations: false,extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/SravanthiArepelly/PipeLine.git']]])
            }
        }
    
    stages{
          stage("maven build"){
            steps{
                sh "mvn clean package"
            }   
        } 
        
        
    }   
}
