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
          step {
              sh 'mvn clean install'
            }
            
          }
        stage('jacoco'){
            steps
            {
            jacoco( 
              execPattern: 'target/*.exec',
			  classPattern: 'target/classes',
			  sourcePattern: 'src/main/java',
			  exclusionPattern: 'src/test*'
           )
            }
          }
       } 
       
    }
