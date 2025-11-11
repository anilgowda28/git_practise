pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/anilgowda28/git_practise.git
            }
        }

        stage('Build WAR File') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Show Files') {
            steps {
                sh 'ls -l target'
            }
        }
    }

    post {
        success {
            echo 'WAR file created successfully inside target folder!'
        }
        failure {
            echo 'Build failed, check console output!'
        }
    }
}
