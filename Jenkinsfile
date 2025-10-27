pipeline {
    agent any

    tools {
        maven 'Maven3'
        jdk 'Java19'
    }

    stages {
        stage('Build') {
            steps {
                bat 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }

        stage('Package') {
            steps {
                bat 'mvn package'
            }
        }

        stage('Run Application') {
            steps {
                bat 'java -cp target/java-jenkins-pipeline-1.0-SNAPSHOT.jar com.example.HelloWorld'
            }
        }
    }

    post {
        always {
            echo 'Pipeline execution completed.'
        }
    }
}
