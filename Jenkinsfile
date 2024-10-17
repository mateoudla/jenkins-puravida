pipeline {
    agent any
    
    stages {
        stage('Clone Repository') {
            steps {
                // Persona 1: Clona el código del repositorio usando SSH
                echo 'Cloning the repository from Git/GitLab...'
                git 'git@github.com:mateoudla/jenkins-puravida.git'
            }
        }

        stage('Build & Test') {
            steps {
                script {
                    // Persona 1: Simulación de construcción del proyecto
                    echo 'Building the project...'
                    sh 'echo "Build successful!"'
                    
                    // Persona 2: Simulación de pruebas unitarias
                    echo 'Running unit tests...'
                    sh 'echo "All tests passed!"'
                }
            }
        }

        stage('Integration Check') {
            steps {
                // Persona 3: Verifica la integración
                echo 'Checking integration...'
                sh 'echo "Integration successful!"'
            }
        }

        stage('Deploy to Testing') {
            steps {
                // Persona 4: Despliega en un entorno de pruebas
                echo 'Deploying to testing environment...'
                sh 'echo "Deployment successful!"'
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline completed!'
        }
    }
}
