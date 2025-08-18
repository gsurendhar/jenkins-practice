pipeline {
    agent any 
    environment {
        COURSE= 'Jenkins'
    }
    options{
        timeout(time:20, unit: 'SECONDS')
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
                    // env 
                    sleep 10
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