pipeline {
     agent {
         node {
             label 'maven-agent'
         }
     }
environment {
    PATH = "/opt/apache-maven-3.9.8/bin:$PATH"
}     
     stages {
         stage('Build') {
             steps {
                sh 'mvn clean deploy'
             }
         }
     }    
}