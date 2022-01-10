pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                echo "dot"
            }
        }
        stage('Test') { 
            steps {
                echo "dot"
            }
        }
        stage('Deploy') { 
            steps {
                echo "dot"
            }
        }
    }
}