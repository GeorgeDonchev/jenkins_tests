pipeline {
    agent none
    stages {
        stage('Build') {
            agent {
                docker { image 'maven:3.8.1-adoptopenjdk-11' }
            }
            steps {
                sh 'mvn --version'
            }
        }
        stage('Deploy') {
            agent {
                docker { image 'node:14-alpine' }
            }
            when {
                expression {
                    currentBuild.result == null || currentBuild.result == 'SUCCESS'
                }
            }
            steps {
                sh 'echo "Deploying..."'
            }
        }
    }
}
