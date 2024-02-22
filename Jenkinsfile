properties([
    buildDiscarder(logRotator(
        artifactDaysToKeepStr: '', 
        artifactNumToKeepStr: '', 
        daysToKeepStr: '', 
        numToKeepStr: '10')), 
    pipelineTriggers([GenericTrigger(
        causeString: 'Generic Cause', 
        regexpFilterExpression: '', 
        regexpFilterText: '', 
        token: 'jenkins-demo', 
        tokenCredentialId: '')]
    )])

node {
    stage('checkout') {
        checkout scmGit(branches: [[name: 'main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/cloudcampla/jenkins-demo']])
    }
    stage('Print Files') {

        sh 'echo "Hello World!"'
        sh 'ls -la'
        sh 'npm install'
    }
}

