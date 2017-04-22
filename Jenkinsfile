pipeline {
    agent any

    stages {
        stage('Install') {
            steps {
                execute 'pip install -r requirements.txt'
            }
        }
        stage('Build') {
            steps {
                execute 'mkdocs build'
            }
        }
        stage('Pack') {
            steps {
                archiveArtifacts artifacts: 'site/**/*.*'
            }
        }
    }
}