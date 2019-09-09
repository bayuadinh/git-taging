pipeline {
    agent { label 'master' }
    environment {
        GIT_TAG = sh(returnStdout: true, script: 'git describe --always').trim()
    }
    stages {
        stage("Testing") {
            when {
                buildingTag()
            }
            environment {
                ENVIRONMENT = 'staging'
            }
            steps {
                sh('cat versiku')
            }
        }
    }
}