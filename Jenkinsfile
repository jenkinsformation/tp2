pipeline {
    agent any
    stages {
        stage('Compile & Tests') {
            parallel {
                stage('Build') {
                    steps {
                        echo "Compile en cours..."
                        sh 'sleep 3' // simulation du build
                    }
                }
                stage('Tests Unitaires') {
                    steps {
                        echo "Execution des tests unitaires..."
                        sh 'sleep 2' // simulation des tests unitaires
                    }
                }
                stage('Analyse quality') {
                    steps {
                        echo "Analyse quality du code..."
                        sh 'sleep 4' // simulation de l'analyse
                    }
                }
            }
        }
    }
}
