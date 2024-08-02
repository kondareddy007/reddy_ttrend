pipeline {
     agent {
         node {
             label 'maven-agent'
         }
     }     
     stages {
         stage('Code pulling') {
             steps {
                echo " We are downloding the code"
                git 'https://github.com/kondareddy007/reddy_ttrend.git'

             }
         }
     }    
}