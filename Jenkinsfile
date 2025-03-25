pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    try {
                        echo "compile started..."
                        sh 'exit 1' // Error simulation
                    } catch(Exception e) {
                        echo "Found an error when building"
                        currentBuild.result = 'FAILURE'
                    }
                }
            }
        }
    }
    post {
        failure {
            echo "Got an error, will send an email"
            sh 'echo "Found error" > erreur.log'
            archiveArtefacts artifacts: 'erreur.log', fingerprint: true
        }
        success {
            echo "Pipeline executed sucessfully"
        }
    }
}
