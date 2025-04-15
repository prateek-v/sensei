pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "test build using webhook "
            }
        }
    }

    post {
        always {
            mail to: 's.sen1996@gmail.com,prateekverma006@gmail.com',
                 subject: "Webhook Build Notification:",
                 body: "Build finished"
        }
    }
}
