pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
                nodejs(nodeJSInstallationName: 'Node 18.4.0'){
                    sh 'npm config set registry http://registry.npmjs.org/'
                    sh 'npm install'
                    sh 'npm run build'
                }
            }
        }
        stage('Test'){
            steps {
                sh 'npm test'
            }
        }
    }
}
