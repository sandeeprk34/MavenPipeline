pipeline {
    agent any 
	
    stages {
        stage('Compile') { 
            steps {
	        withMaven(maven : 'mymaven') {
		     sh 'mvn clean compile'
	        }
                
            }
        }
        stage('Test') { 
            steps {
	       withMaven(maven : 'mymaven') {
	           sh 'mvn test'
               }
            }
        }
        stage('Deploy') { 
            steps {
                withMaven(maven : 'mymaven') {
	             sh 'mvn deploy'
            }
        }
    }

   }
}

