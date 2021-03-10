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
       } 
       
    }
