pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG20CS259_task5 PES1UG20CS259_task5.cpp'
                build job: 'PES1UG20CS259-1'
            }
        }
        
        stage('Test') {
            steps {
                sh './PES1UG20CS259_task'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deployment'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
