
pipeline {
    triggers {
  pollSCM('* * * * *')
    }
   agent any
    tools {
  maven 'M2_HOME'
  }

 

    stages {

        stage("build & SonarQube analysis") {          
            steps {
                    withSonarQubeEnv('sonar') {
                        sh 
                    }
             
            }
        }

        

         stage("Maven Build Back-End") {
            steps {
                echo 'Build Back-End Project...'
                    script {
                    sh "mvn package -DskipTests=true"
                    }
             
            }
        }

    }