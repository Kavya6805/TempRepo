pipeline{
    agent any
    stages{
        stage('Pipeline started'){
            steps{
                echo "pipeline started."
            }
        }
        stage('Identify Branch'){
            steps{
                script{
                    def runningBranch = env.GIT_BRANCH

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
        stage('Pipeline ended'){
            steps{
                echo "pipeline ended."
            }
        }
    }
}