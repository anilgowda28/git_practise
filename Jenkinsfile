pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Pull latest code from GitHub
                git branch: 'main', url: 'https://github.com/anilgowda28/git_practise.git
            }
        }

        stage('Compile') {
            steps {
                echo 'Compiling C program...'
                sh '''
                    gcc hello.c -o hello
                '''
            }
        }

        stage('Run') {
            steps {
                echo 'Running compiled program...'
                sh './hello'
            }
        }

        stage('Post-Build') {
            steps {
                echo 'Build and run completed successfully.'
            }
        }
    }

    post {
        failure {
            echo '❌ Build failed!'
        }
        success {
            echo '✅ Build succeeded!'
        }
    }
}
