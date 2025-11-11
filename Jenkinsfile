pipeline {
    agent any

    stages {
        stage('Build WAR') {
            steps {
                sh 'mvn clean package'
            }
        }
    }

    post {
        success {
            echo 'WAR file created in target folder!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}
