pipeline {
    agent any
    
    tools {
        maven 'mvn.3.9.9'
        jdk 'jdk17'
    }
    
    stages {
        stage('Clean y Test') {
            steps {
                sh 'mvn clean test -B -ntp'
            }
            post {
                // ✅ Publica los resultados para ver qué pruebas fallaron
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
        
        stage('Build') {
            steps {
                // Si las pruebas fallaron, esto no se ejecutará
                sh 'mvn package -B -ntp'
            }
        }
    }
    
    post {
        always {
            cleanWs()
        }
    }
}