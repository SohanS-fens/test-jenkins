pipeline {
    agent any
    
    environment {
        AWS_CREDENTIALS_ID = credentials('33a27540-5ce7-469c-9155-8e660f98fd92')
    }

    stages {

        stage('Run Script') {
            steps {
                script {
                  bat 'bash script.sh all plan'
                }
            }
        }
    }
}
