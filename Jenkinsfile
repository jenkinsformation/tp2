pipeline {
    agent any
    environment {
        DOCKER_USER = 'dockerdavetp3'
    }
    stages {
        stage('Login Docker') {
            steps {
                script {
                    withCredentials([string(credentialsId:'DOCKER_PASSWORD_DB', variable: 'DOCKER_PASS')])
                    {sh 'echo $DOCKER_PASS | docker login -u $DOCKER_USER --password-stdin'}
                    echo "Building ${APP_NAME} version ${buildVersion}"
                }
            }
        }
    }
}
