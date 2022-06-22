pipeline {
    agent any
    tools {
        nodejs 'LTS'
    }
    stages {
        stage('Information'){
            steps {
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
                sh 'npm -v'
                sh 'node -v'
                sh 'whoami'
            }
        }
        stage('Build') {
            steps {
                sh 'npm cache verify'
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
