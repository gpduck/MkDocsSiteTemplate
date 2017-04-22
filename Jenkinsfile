pipeline {
    agent any

    stages {
        stage('Install') {
            steps {
                script {
                    execute 'pip install -r requirements.txt'
                }
            }
        }
        stage('Build') {
            steps {
                script {
                    execute  'mkdocs build'
                }
            }
        }
        stage('Pack') {
            steps {
                archiveArtifacts artifacts: 'site/**/*.*'
            }
        }
    }
}