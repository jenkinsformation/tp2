pipeline {
    agent any
    environment {
        DOCKER_USER = 'ferrenzio@gmail.com'
    }
    stages {
        stage('Login Docker') {
            steps {
                script {
                    withCredentials([string(credentialsId:'DOCKER_PASSWORD_DB', variable: 'DOCKER_PASS')])
                    {sh 'echo $DOCKER_PASS | docker login -u $DOCKER_USER --password-stdin'}
                }
            }
        }
    }
}
