pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh "./mvnw verify"
                // how to expose template parameters such as "$recipient"
                mail body: 'build successful', subject: "$name repository", to: "$recipient"

            }
        }
    }
}