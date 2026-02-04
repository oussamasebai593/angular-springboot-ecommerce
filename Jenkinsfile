pipeline {
    agent any

    tools {
        jdk 'JDK17'
        maven 'maven'
    }

    stages {
        stage('Git checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/oussamasebai593/angular-springboot-ecommerce.git'
            }
        }
    stage('Compile') {
        steps {
            dir('backend') {
            sh 'mvn clean compile'
        }
            }
        }
    }
}


