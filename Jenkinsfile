pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/SohanS-fens/test-jenkins.git']])
            }
        }

        stage('Run Script') {
            steps {
                // Make the script executable and run it with the required arguments
                bat 'script.sh iam_user_all_rules_violation apply'
            }
        }
    }

}
