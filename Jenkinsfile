pipeline {

    agent any

    environment {
        DOCKER_IMAGE = "darm1234/spring-petclinic:latest"
    }

    stages {

        stage('Clone') {
            steps {
                git 'https://github.com/Deibytin/spring-petclinic.git'
            }
        }

        stage('Build') {
            steps {
                sh './mvnw clean package -DskipTests'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t $DOCKER_IMAGE .'
            }
        }

        stage('Finish') {
            steps {
                echo 'Finished: SUCCESS'
            }
        }
    }
}
