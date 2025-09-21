pipeline {
    agent any
    tools {
        maven 'maven_3.8.6'
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package -DskipTests'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                // Example: run the JAR (replace with your real deploy step)
                sh 'nohup java -jar target/*.jar &'
            }
        }
    }
} 