pipeline {
    agent any

    stages {
        stage('Install') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Build') {
            steps {
                sh 'mkdocs build'
            }
        }
        stage('Pack') {
            archiveArtifacts artifacts: 'site/**/*.*'
        }
    }
}