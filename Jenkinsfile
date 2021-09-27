@Library("Shared-library") _
currentBuild.displayName = "${currentBuild.projectName}#${currentBuild.number}"
pipeline {
    agent any 
    tools {
        // Note: this should match with the tool name configured in your jenkins instance (JENKINS_URL/configureTools/)
        nodejs "node"
    }
        stages {
            stage ("git code checkout"){
            steps{
                echo "get source code"
                git changelog: false, credentialsId: 'git_creds', poll: false, url: 'https://github.com/jinjadarkwebjinja/node-hello.git'
                echo 'scm is done guys!'
            }
        }
            stage ("Build"){
            steps{
                sampletest()
            }
            }
              stage ("Env Build Number"){
            steps{
            sampletest()
            }
  }
  stage('Build Status Through Email Notification'){
            steps{
            mail bcc: 'sridhar.vimala@infosys.com', body: ''' Thanks,
Sangi Mangi & Mangi Sangi''', cc: 'jinjajenkinsuser@gmail.com', from: '', replyTo: '', subject: "${env.JOB_NAME}" , to: ''
}
  }
}
        }
