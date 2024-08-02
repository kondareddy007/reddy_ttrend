pipeline {
    agent {
        node {
            label 'maven-agent'
         }
     }     
    stages {
        stage('Clone code') {
            steps {
             echo " We are downloding the code"
             git branch: 'master', url: 'https://github.com/kondareddy007/reddy_ttrend.git'

            }
         }
     }    
}