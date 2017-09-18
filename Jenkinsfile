node {
    checkout scm
    stage('Build Image') {
        ansiColor('xterm') {
            sh 'packer build -var-file=/etc/packer.d/vsphere_creds.json main.json'
            build job: '../tomcat/master', wait: false
        }
    }
}
