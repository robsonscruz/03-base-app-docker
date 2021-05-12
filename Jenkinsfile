pipeline {
    agent any

    stages{
        stage('Clone') {
            steps {
                script {
                    checkout scm
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    sh 'rm -rf .git .gitignore Jenkinsfile README.md /app/*';
                    sh 'cp -r ./* /app/';
                }
            }
        }
    }
}