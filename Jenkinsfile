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
         stage('build') {
            steps {
                sh "mvn clean package -DskipTests=true"
            }
        }
    }
}
