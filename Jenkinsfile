pipeline {
    agent any

    stages {
        stage('git checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/repo19352/my-project.git'
            }
        }
         stage('compile') {
            steps {
                sh "mvn clean compile"
            }
        }
         stage('test') {
            steps {
                sh "mvn clean test"
            }
        }
         stage('build') {
            steps {
                sh "mvn clean package"
            }
        }
    }
}
