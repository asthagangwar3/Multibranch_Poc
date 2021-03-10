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
        } 
       
    }
