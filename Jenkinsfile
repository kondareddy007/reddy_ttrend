pipeline {
    agent {
        node {
            label 'maven-agent'
         }
     }
     environment {
        PATH = "/opt/maven/bin:$PATH"
     }     
    stages {
        stage('Build code') {
            steps {
            echo '------------------- Build Started -------------'
                sh 'mvn clean deploy -Dmaven.test.skip=true'
                echo '------------------- Build Completed -------------'
            }
         }

         stage('Unit Test') {
            steps{
                echo '------------------- Unit Test Started -------------'
                sh 'mvn surefire-report:report'
                echo '------------------- Unit Test Completed -------------'
            }
         }
    }
}

