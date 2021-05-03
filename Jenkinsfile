pipeline {
    agent {
        label 'master' 
          }
  
    stages {
        stage('build') {
            steps
                {
                 bat 'mvn install -Dmaven.test.skip=true'
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
