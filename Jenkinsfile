pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checkout github'
                checkout([$class: 'GitSCM', branches: [[name: '*/python']], extensions: [], userRemoteConfigs: [[credentialsId: 'd12fc0a9-7f92-4ca0-87d3-5169b3e06670', url: 'https://github.com/Arczi-pl/easy-jenkins-python-pipeline.git']]])
            }
        }
        stage('Build') {
            steps {
                git branch: 'python', credentialsId: 'd12fc0a9-7f92-4ca0-87d3-5169b3e06670', url: 'https://github.com/Arczi-pl/easy-jenkins-python-pipeline.git'
                sh 'python time-since-epoch.py'
            }
        }
        stage('Test') {
            steps {
                echo 'It might be tested'
            }
        }
    }
}
