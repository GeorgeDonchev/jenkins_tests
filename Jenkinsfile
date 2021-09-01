pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello world"'
                sh '''
                    echo "Multiple shell steps works too"
                '''
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Testing..."'
                sh 'ehoc "Still testing..."'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploying..."'
            }
        }
    post {
        always {
            echo 'This always run....'
        }
        success {
            echo 'This alway run successful...'
        }
    }
    }
}
