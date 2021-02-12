node('master') {
    stage("Fetch Source Code") {
        git 'https://github.com/harikahappy/python-jenkins-pipeline'
    }
    
        stage("Testing") {
            sh 'python test_functions.py'
        }
        stage("Deployment") {
            if (env.BRANCH_NAME == 'master') {
                printMessage('Deploying the master branch')
            } else {
                printMessage("No deployment for branch [${env.BRANCH_NAME}]")
            }
            
        }
        printMessage('Pipeline Complete')
   
}

def printMessage(message) {
    echo "${message}"
}
