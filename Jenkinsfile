pipeline {
    agent any
    tools {
        maven 'maven_3_0_5'
    }
    stages {
        stage ('Compile Stage') {

            steps {                
                    bat 'mvn clean compile'                
            }
        }

        stage ('Testing Stage') {

            steps {                
                    bat 'mvn test'                
            }
        }
         stage('results') {
            junit '**/target/surefire-reports/TEST-*.xml'
        }       
    }    
}
