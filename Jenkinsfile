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
        dir 'site'
        if(isUnix()) {
            sh 'tar -cf ../${JOB_BASE_NAME}-${BUILD_NUMBER}.tar ./*'
        } else {
            bat "powershell 'compress-archive -DestinationPath ..\${env:JOB_BASE_NAME}-${env:BUILD_NUMBER}.zip' -Path .\"
        }
        archiveArtifacts artifacts: '*.zip,*.tar'
    }
}