pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                bat "rmdir -p jenkins_test"
                bat "git clone git@github.com:amr158/jenkins_test.git"
                bat "mvn clean -f jenkins_test"
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