pipeline {
    agent {
        dockerfile true
    }

    stages {
        stage('Test') {
            steps {
                echo "Test started"
                sh 'python3 -V'
            }
        }
        stage('Checkout Code') {
            steps {
                echo "Checkout Code started"
            }
        }
        stage('Build') {
            steps {
                echo "Build started"
                docker.build("jr/web-python-flask:${env.BUILD_ID}")
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploy started"
                docker.image("jr/web-python-flask:${env.BUILD_ID}").withRun('-p 8080:80') {
                    
                }
            }
        }
    }
}
