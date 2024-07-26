pipeline {
    agent any
    
    stages {

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
