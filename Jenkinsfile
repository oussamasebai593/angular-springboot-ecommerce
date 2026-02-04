pipeline {
    agent any

    environment {
        DOCKER_IMAGE = "backend:latest"
    }

  

        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker build -t $DOCKER_IMAGE .'
                }
            }
        }

        stage('Run Tests') {
            steps {
                script {
                    // Si tu as des tests Maven
                    sh 'docker run --rm $DOCKER_IMAGE mvn test'
                }
            }
        }

        stage('Docker Compose Up') {
            steps {
                script {
                    sh 'docker-compose up -d --build'
                }
            }
        }

        stage('Docker Compose Down') {
            steps {
                script {
                    sh 'docker-compose down'
                }
            }
        }
    }

    post {
        always {
            echo 'Pipeline terminé'
        }
    }
}

