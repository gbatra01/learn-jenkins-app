pipeline {
    agent any
    stages {
        /*
        stage('Build') {
            // This is a comment.
         agent {
                docker {
                    image 'node:18-alpine'
                    reuseNode true
                    }
              }
            steps {
                sh '''
                ls -la
                node --version
                npm --version
                npm ci
                npm run build
                ls -la
                '''
            }
        }
        */
             stage ('Test') {
                    /* This is first comment
                        This is second comment
                    */
                agent {
                    docker {
                        image 'node:18-alpine'
                        reuseNode true
                    }
                }
                steps {
                    sh '''
                    test -f build/index.html             
                    npm test
                    '''
                }      
        }
    }
    post {
        always {
            junit 'test-results/junit.xml'

        }

    }
}

