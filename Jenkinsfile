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
        }
}
