pipeline {
    agent any

    stages {
        stage('clone repo and clean it') {
            steps {
                bat "git clone https://github.com/Manoj-T529/spring-jenkins.git"
                bat "mvn clean -f spring-jenkins"
            }
        }
        
         stage('Test') {
            steps {
                bat "mvn test -f spring-jenkins"
            }
        }
        
         stage('Deploy') {
            steps {
                bat "mvn package -f spring-jenkins"
            }
        }
    }
}
