pipeline {
    agent any

    stages {
        stage('Build/Interpreter') {
            steps {
                sh echo "FUNCIONOU"
                python hello.py
            }
        }
        stage('Send SinaldeFumaca'){
            steps {
                echo 'E-mail enviado no pós-build deste job'
            }
        }
    }
}