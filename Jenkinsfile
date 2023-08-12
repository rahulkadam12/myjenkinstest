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
        stage('Yum Update') {
            steps {
                sh 'sudo yum update -y'
            }
        }
    }
}
