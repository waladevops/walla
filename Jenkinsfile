pipeline {
    agent any

    stages {
        stage('checkout') {
            steps {
                echo 'checkout code'
                git(url: 'https://github.com/ymnajja/jenkins.git', branch: 'master')
            }
        }
        stage('Build') {
            steps {
                echo 'building'
                sh 'npm install'
            }
        }
        stage('Build image') {
            steps {
                echo 'building image'
                sh 'docker build -t test .'
            }
        }
        
        }
    }
}

