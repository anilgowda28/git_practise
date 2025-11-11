pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                echo 'Pulling code from GitHub...'

                git branch: 'main', url: 'https://github.com/anilgowda28/git_practise.git'
            }
        }

        stage('List Files') {
            steps {
                echo 'Listing files from repository...'
                sh 'ls -l'
            }
        }
    }

    post {
        success {
            echo '✅ Code pulled successfully from GitHub!'
        }
        failure {
            echo '❌ Failed to pull code from GitHub.'
        }
    }
}
