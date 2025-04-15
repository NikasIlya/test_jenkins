pipeline {
     agent {
        docker { image 'python:3.10-slim' }
    }
    stages {
        stage('Checkout') {
            steps {
                git url:'https://github.com/NikasIlya/test_jenkins.git', branch: 'main'
            }
        }
        stage('Install') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                sh 'pytest'
            }
        }
    }
}
