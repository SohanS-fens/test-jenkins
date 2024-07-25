pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the GitHub repository
                git url: 'https://github.com/SohanS-fens/test-jenkins', credentialsId: '7c71b585-c11b-43fe-97e1-6d568ef38d1d'
            }
        }

        stage('Run Script') {
            steps {
                // Make the script executable and run it with the required arguments
                bat 'script.sh all plan'
            }
        }
    }

}
