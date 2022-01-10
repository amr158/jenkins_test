pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh "git clone https://github.com/amr158/jenkins_test.git"
                sh "mvn clean -f jenkins_test"
            }
        }
        stage('Test') { 
            steps {
                bat "mvn test -f jenkins_test"
            }
        }
        stage('Deploy') { 
            steps {
                bat "mvn package -f jenkins_test"
            }
        }
    }
}