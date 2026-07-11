pipeline {
    agent any
    
    tools {
        // ✅ Correcto - Coincide con tu configuración
        maven 'mvn.3.9.9'
        jdk 'jdk17'
    }
    
    stages {

        stage('Compile') {
            steps {
                // Usamos test
                sh 'mvn clean compile -B -ntp'
            }
        }
		stage('Test') {
            steps {
                // Usamos test
                sh 'mvn test -B -ntp'
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