pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o PES2UG22CS663-1 SRNmain.cpp' // Replace 'YOUR_SRN-1' with your actual SRN
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './PES2UG22CS663-1' // Running the compiled binary
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'Deploying the application...'
                    // Add deployment steps here, e.g., copy files, upload, etc.
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
