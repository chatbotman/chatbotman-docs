pipeline {
    agent any

    environment {
        EMAIL = 'chatbotman.dev@proactivesystem.com.hk'
    }

    stages {
        stage('Deploy') {
            agent {
                docker {
                    image 'proactivehk/docker-hexo'
                    // args "-u root"
                }
            }
            steps {
                sh "pwd"
                sh "hexo deploy --generate"
            }
        }
    }

    post {
        always {
            emailext(body: '${DEFAULT_CONTENT}', mimeType: 'text/html',
                    replyTo: '$DEFAULT_REPLYTO', subject: '${DEFAULT_SUBJECT}',
                    to: "${env.EMAIL}")
        }
    }
}