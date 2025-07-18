pipeline {
    agent any

    stages {
        stage('Build Java (Maven)') {
            steps {
                script {
                    docker.image('maven:3.9-eclipse-temurin-17').inside {
                        dir('java-app') {
                            sh 'mvn clean install'
                        }
                    }
                }
            }
        }
    }
}
