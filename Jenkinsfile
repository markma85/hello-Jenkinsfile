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
                //def customImage = docker.build("jr/web-python-flask")
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploy started"

            }
        }
    }
}
