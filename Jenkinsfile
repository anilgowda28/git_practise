pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/anilgowda28/git_practise.git
            }
        }

        stage('Build WAR') {
            steps {
                sh 'mvn clean package'
            }
        
        }
    }
}
