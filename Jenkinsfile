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
            mail to: 's.sen1996@gmail.com','prateekverma006@gmail.com'
                 subject: "Webhook Build Notification: ${JOB_NAME} - Build #${BUILD_NUMBER}",
                 body: """
                 This is a notification for build #${BUILD_NUMBER} of the job ${JOB_NAME}.

                 Build Status: ${BUILD_STATUS}

                 Check the build console output for more details: ${BUILD_URL}
                 """
        }
    }
}
