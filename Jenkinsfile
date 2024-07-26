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
                bat 'bash -c "bash script.sh 0 plan"'
            }
        }
    }

}
