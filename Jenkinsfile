pipeline {
    agent any 
    environment {
        COURSE= 'Jenkins'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                sh """
                    echo 'Testing..'
                    env 
                """
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
            deleteDir()
        }
        success {
            echo 'Pipeline was Success'
        }
        failure {
            echo 'Pipeline was Failure'
        }
    }
}