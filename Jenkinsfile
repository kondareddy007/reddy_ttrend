pipeline {
    agent {
        node {
            label 'maven-agent'
         }
     }
     environment {
        PATH = "/opt/apache-maven-3.9.8/bin"
     }     
    stages {
        stage('Clone code') {
            steps {
                // sh 'mvn clean install'
		sh 'helloworld'
                echo "testing on multibranch pipeline"
            }
         }
     }    
}

