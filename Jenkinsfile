pipeline {
    agent any
    
    tools {
        // ✅ Correcto - Coincide con tu configuración
        maven 'mvn.3.9.9'
    }
    
    stages {
        // 1. Compilar
        stage('Compile') {
            steps {
                sh 'mvn clean compile -B -ntp'
            }
        }
        
        // 2. Probar (AQUÍ FALLAN LAS PRUEBAS)
        stage('Test') {
            steps {
                sh 'mvn test -B -ntp'
            }
            post {
                // Publicar resultados aunque fallen
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
        
        // 3. Empaquetar (se salta porque falló Test)
        stage('Build') {  // ← Corregido: "Build" en lugar de "Buils"
            steps {
                sh 'mvn package -DskipTests -B -ntp'
            }
        }
    }
    
    post {
        always {
            cleanWs()
        }
    }
}