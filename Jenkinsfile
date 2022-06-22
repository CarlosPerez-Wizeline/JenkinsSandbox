pipeline {
    agent any
    tools {
        nodejs 'LTS'
    }
    stages {
        stage('Build') {
            steps {
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
