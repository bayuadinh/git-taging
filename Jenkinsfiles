pipeline {
    agent any
    stages {
        stage('Date') {
            steps {
                sh 'date'
            }
        }
        stage('Deploy') {
            when { tag "RC-*" }
            steps {
                echo 'Deploying only because this commit is tagged...'
                cat 'versiku'
            }
        }
    }
}