pipeline {
    agent {
        label 'jenkins-slave'
    }
    
    stages {
        stage('Hello') {
            steps {
                sh 'echo "Hello, World!"'
            }
        }
        stage('Install wget') {
            steps {
                sh 'sudo yum install wget -y'
            }
        }
    }
}
