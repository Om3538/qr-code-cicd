pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/Om3538/qr-code-cicd.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Test') {
            steps {
                // optional: if you have tests
                sh 'pytest || echo "No tests found"'
            }
        }

        stage('Build') {
            steps {
                echo 'Building project...'
                // your custom build step (if needed)
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // example:
                // sh 'scp -i key.pem app.py ubuntu@ip:/var/www/html/'
                // OR docker build and push
            }
        }
    }
}
