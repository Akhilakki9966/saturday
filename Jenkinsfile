pipeline {
    agent any
    environment {
        PATH = "/home/akhil/apache-maven-3.9.9/bin:$PATH"
    }
    stages{
        stage ('checkout') {
            steps {
                git branch :'main', url : 'https://github.com/Akhilakki9966/saturday.git'
            }
        }
        stage ('clean') {
            steps {
                sh 'mvn clean'
            }
        }
        stage('install') {
            steps {
                sh 'mvn install'
            }
        }
        stage ('package') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
