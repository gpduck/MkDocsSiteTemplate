pipeline {
    agent any

    stages {
        stage('Install') {
            steps {
                if(isUnix()) {
                    sh 'pip install -r requirements.txt'
                } else {
                    bat 'pip install -r requirements.txt'
                }
            }
        }
        stage('Build') {
            steps {
                if(isUnix()) {
                    sh 'mkdocs build'
                } else {
                    bat 'mkdocs build'
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