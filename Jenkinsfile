pipeline {
    agent any

    stages {
        stage('Install') {
            steps {

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