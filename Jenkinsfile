pipeline {
    agent {
        docker {
            image 'node:18-alpine'
        }
    }
    stages {
        stage('Install Netlify CLI') {
            steps {
                sh 'npm ci'
                sh 'npm install netlify-cli'
                sh 'npm --version'
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
