pipeline {
    agent {
        node {
            label 'maven-agent'
         }
     }
     /*environment {
        PATH = "/opt/maven/bin:$PATH"
     }*/
     tools {
        maven 'M3'
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
          stage('SonarQube analysis') {
            environment {
            scannerHome = tool 'Valaxy-SonarScanner'
            }
        steps { 
            echo '------------------- Sonar Started -------------'
        withSonarQubeEnv('Valaxy-SonarQube-Server') { // If you have configured more than one global server connection, you can specify its name
            sh "${scannerHome}/bin/sonar-scanner"
    }
    echo '------------------- Sonar Analysis Completed -------------'
    }
    }
 }
}

