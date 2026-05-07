pipeline{
    agent any
    stages{
        stage('Identify Branch'){
            steps{
                script{
                    def runningBranch = env.BRANCH_NAME ?: env.GIT_BRANCH ?: "Unknown Branch"

                    def startTime = new Date(currentBuild.startTimeInMillis).toString()

                    def buildVersion = env.BUILD_NUMBER

                    echo """
                    -----------------------------------------
                    Release Status:
                    - Branch:  ${runningBranch}
                    - Started: ${startTime}
                    - Version: ${buildVersion}
                    -----------------------------------------
                    """
                }
            }
        }
    }
}