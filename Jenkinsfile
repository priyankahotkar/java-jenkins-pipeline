pipeline {
    agent any

    tools {
        maven 'Maven3'
        jdk 'Java19'
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/priyankahotkar/java-jenkins-pipeline.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test || true'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }

        stage('Run Application') {
            steps {
                sh 'java -jar target/java-jenkins-pipeline-1.0-SNAPSHOT.jar'
            }
        }
    }

    post {
        always {
            echo 'Pipeline execution completed.'
        }
    }
}
