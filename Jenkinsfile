pipeline {
    agent any

    stages {

        stage('Install Frontend') {
            steps {
                dir('frontend') {
                    sh 'npm install'
                }
            }
        }

        stage('Build Frontend') {
            steps {
                dir('frontend') {
                    sh 'npm run build'
<<<<<<< HEAD
=======
                }
            }
        }stage('Backend Build') {
            steps {
                dir('backend') {
                    sh './mvnw clean package -DskipTests'
>>>>>>> 64ea8b3 (Merge local work after pull)
                }
            }
        }

<<<<<<< HEAD
        stage('Backend Build') {
            steps {
                dir('backend') {
                    sh './mvnw clean package -DskipTests'
                }
            }
        }

=======
>>>>>>> 64ea8b3 (Merge local work after pull)
    }

    post {
        always {
            echo "Pipeline terminé"
        }
    }
}
