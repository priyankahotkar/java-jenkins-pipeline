pipeline {
    agent any

    tools {
        maven 'Maven3'
        jdk 'Java19'
    }

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }

        stage('Run Application') {
            steps {
                sh 'java -cp target/java-jenkins-pipeline-1.0-SNAPSHOT.jar com.example.HelloWorld'
            }
        }
    }

    post {
        always {
            echo 'Pipeline execution completed.'
        }
    }
}
