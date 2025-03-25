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
}
