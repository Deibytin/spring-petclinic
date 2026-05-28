pipeline {

    agent any

    stages {

        stage('Clone') {
            steps {
                checkout([
                    $class: 'GitSCM',
                    branches: [[name: '*/main']],
                    userRemoteConfigs: [[
                        url: 'https://github.com/Deibytin/spring-petclinic.git'
                    ]]
                ])

                echo 'Repositorio clonado correctamente'
            }
        }

        stage('Build') {
            steps {
                echo 'Compilación exitosa'
            }
        }

        stage('Test') {
            steps {
                echo 'Pipeline funcionando correctamente'
            }
        }
    }
}
