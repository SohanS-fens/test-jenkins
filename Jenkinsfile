pipeline {
    agent any
    
    environment {
        AWS_ACCESS_KEY_ID = credentials('aws-access-key-id')
        AWS_SECRET_ACCESS_KEY = credentials('aws-secret-access-key')
    }

    stages {
        
        stage('AWS CLI Test') {
            steps {
                sh 'aws sts get-caller-identity'
            }

        stage('Run Script') {
            steps {
                script {
                    // Check if the script exists
                    if (fileExists('script.sh')) {
                        // Execute the Bash script using Git Bash
                        bat '"C:\\Program Files\\Git\\bin\\bash.exe" -c "bash script.sh 0 plan"'
                    } else {
                        error 'script.sh not found'
                    }
                }
            }
        }
    }
}
