pipeline {
    agent any
    tools {
        maven 'Maven'
        jdk 'Java_11'
            }
    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/anilgowda28/git_practise.git'
            }
        }

        stage('Build clean') {
            steps {
                sh 'mvn clean'
            }
        }

        stage('Maven Build') {
            steps {
                sh 'mvn clean install'
            }
        }
    }