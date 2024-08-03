pipeline {
    agent {
        node {
            label 'maven-agent'
         }
     }
     environment {
        PATH = "/opt/maven/bin:$PATH "
     }     
    stages {
        stage('Build code') {
            steps {
              sh 'mvn clean install'
		  //sh 'helloworld'
                echo "testing on multibranch pipeline"
            }
         }
     }    
}

