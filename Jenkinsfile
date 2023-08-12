pipeline {
    agent {
        label 'jenkins-slave'
    }
    
    parameters {
        booleanParam(name: 'RUN_YUM_UPDATE', defaultValue: true, description: 'Run yum update?')
        string(name: 'COMMENT', defaultValue: '', description: 'Comment to include')
    }
    
    stages {
        stage('Print Comment') {
            steps {
                script {
                    if (params.COMMENT) {
                        echo "Comment provided: ${params.COMMENT}"
                    } else {
                        echo "No comment provided."
                    }
                }
            }
        }
        
        stage('Yum Update') {
            when {
                expression { params.RUN_YUM_UPDATE }
            }
            steps {
                sh 'sudo yum update -y'
            }
        }
    }
}
