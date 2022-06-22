pipeline {
    agent { label 'linux'}
    tools {
        nodejs 'LTS'
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
                sh 'npm run build'
            }
        }
        stage('Test'){
            steps {
                sh 'npm test'
            }
        }
    }
}
