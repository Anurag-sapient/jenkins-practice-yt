pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
               //bat "rmdir  /s /q TicketBookingServiceJunitTesting"
                bat "git clone https://github.com/Anurag-sapient/jenkins-practice-yt.git"
                bat "mvn clean -f jenkins-practice-yt"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f jenkins-practice-yt"
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f jenkins-practice-yt"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f jenkins-practice-yt"
            }
        }
    }
}
