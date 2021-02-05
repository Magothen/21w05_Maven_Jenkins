pipeline {
    agent any
    stages{
        stage('Checkout'){
            steps {
                git 'https://github.com/Magothen/21w05_Maven_Jenkins.git'
            }
        }
        stage('Build') {
            steps {
                bat "mvn compile"
            }
        }
        stage('Test') {
            steps {
                bat "mvn test"
            }
            post {
                always {
                    junit '**/TEST*.xml'
                }
            }
        }
    }
}
