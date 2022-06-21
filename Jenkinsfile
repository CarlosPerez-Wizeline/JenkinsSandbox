pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
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
