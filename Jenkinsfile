pipeline {
    agent any
    
    stages {
        stage('Clone Repository') {
            steps {
                echo 'Clonando el repositorio desde GitHub...'
                git 'git@github.com:mateoudla/jenkins-puravida.git'
            }
        }

        stage('Construcción y prueba') {
            steps {
                script {
                    echo 'Construyendo el proyecto....'
                    sh 'echo "Construcción completa!"'
                    
                    echo 'Corriendo pruebas unitarias....'
                    sh 'echo "Pruebas aprobadas!"'
                }
            }
        }

        stage('Verificación de integración') {
            steps {
                echo 'Verificando la integración...'
                sh 'echo "Integración correcta!"'
            }
        }

        stage('Despliegue de entorno de pruebas') {
            steps {
                echo 'Desplegando el entorno de pruebas...'
                sh 'echo "Despliegue correcto!"'
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline completado!'
        }
    }
}
