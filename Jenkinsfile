pipeline {
    agent any
    stages {
        stage('Install Netlify CLI') {
            steps {
                sh 'npm install netlify-cli'
                sh 'netlify --version'
            }
        }
        stage('Build Application') {
            steps {
                sh 'npm run build'
                 }
        }
    }
}
