pipeline {
    agent any

    stages {
        stage('Build/Interpreter') {
            steps {
                echo 'FUNCIONOU'
                sh 'python hello.py'
            }
        }
        stage('Send SinaldeFumaca'){
            steps {
                echo 'E-mail enviado no pós-build deste job'
            }
        }
    }
    post {
        always {
            emailext body: 'Joob de build hello.py finalizado com sucesso!', recipientProviders: [[$class: 'DevelopersRecipientProvider'], [$class: 'RequesterRecipientProvider']], subject: 'Job de teste finalizado com sucesso'
        }
    }
}