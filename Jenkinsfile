node {
    stage('Install') {
        if(isUnix()) {
            sh 'pip install -r requirements.txt'
        } else {
            bat 'pip install -r requirements.txt'
        }
    }
    stage('Build') {
        if(isUnix()) {
            sh 'mkdocs build'
        } else {
            bat 'mkdocs build'
        }
    }
    stage('Pack') {
        archiveArtifacts artifacts: 'site/**/*.*'
    }
}