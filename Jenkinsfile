@"
pipeline {
    agent any

    tools {
        maven 'Maven'
    }

    stages {

        stage('Build') {
            steps {
                echo 'Building the project...'
                bat 'mvn compile'
            }
        }

        stage('Test') {
            steps {
                echo 'Running test cases...'
                bat 'mvn test'
            }
        }

        stage('Package') {
            steps {
                echo 'Packaging into JAR...'
                bat 'mvn package'
            }
        }
    }

    post {
        success {
            echo 'BUILD SUCCESSFUL!'
        }
        failure {
            echo 'BUILD FAILED!'
        }
    }
}
"@ | Out-File -FilePath "Jenkinsfile" -Encoding utf8