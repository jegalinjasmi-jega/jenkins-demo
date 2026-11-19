
pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Building the project'
                sh 'ls -l'
                sh 'test -f index.html'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing the project'
                sh 'grep -q "Welcome to DevOps!" index.html'
                echo 'Test Passed!'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the project'
                sh 'mkdir -p /tmp/jenkins-demo-deploy'
                sh 'cp index.html /tmp/jenkins-demo-deploy/'
                echo 'Deployment Successful!'
            }
        }
    }
}
