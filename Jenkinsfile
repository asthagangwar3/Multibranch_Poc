pipeline {
    agent {
        label 'master' 
          }
  
    stages {
        stage('build') {
            steps
                {
                 sh 'mvn install -Dmaven.test.skip=true'
                }
            }
        stage('test'){
          steps {
              sh 'mvn clean install'
            }
            
          }
        stage('jacoco'){
            steps
            {
            jacoco()
            }
          }
        stage('sonar'){
          steps
            {
                withSonarQubeEnv(installationName:'Sonar' , credentialsId: 'sonar_secret_new')
                {
                 sh 'mvn clean install sonar:sonar'
                }
            }
            
        }
       } 
       
    }
