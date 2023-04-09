pipeline {
    agent any 
    stages {
        stage('Clone Repo and Clean') { 
            steps {
                sh "rm -rf my-app"
                sh "git clone https://github.com/V-vk-404/my-app.git "
                sh "mvn clean -f my-app"
            }
        }
        stage('Test') { 
            steps {
                sh "mvn test -f my-app" 
            }
        }
        stage('Deploy') { 
            steps {
                sh "mvn package -f my-app"
            }
        }
    }
}
