pipeline {
    agent any
    
    tools {
        // ✅ Correcto - Coincide con tu configuración
        maven 'mvn.3.9.9'
        jdk 'jdk17'
    }
    
    stages {
        stage('Test') {
            steps {
                // Usamos test
                sh 'mvn clean test -B -ntp'
            }
        }
        stage('Buils') {
            steps {
                // Usamos test
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