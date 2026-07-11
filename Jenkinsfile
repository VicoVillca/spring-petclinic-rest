pipeline {
    agent any
    
    tools {
        // ✅ Correcto - Coincide con tu configuración
        maven 'mvn.3.9.9'
        jdk 'jdk17'
    }
    
    stages {

        stage('Buils') {
            steps {
                // Usamos test
                sh 'mvn --version'
            }
        }
    }
    
    post {
        always {
            cleanWs()
        }
    }
}