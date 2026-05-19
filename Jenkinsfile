pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                image 'node:18-alpine'
                reuseNode true
            }
            steps {
                sh '''
                    ls -la
                    node --version
                    nmp --version
                    npm ci
                    npm run build
                    ls -la
                '''
            }
        }
    }
}
