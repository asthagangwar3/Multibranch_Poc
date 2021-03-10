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
        } 
       
    }
