@Library("mylibrary")_
node('built-in')
{
    stage('ContDownloa_Master')
    {
        cicd.newGit("https://github.com/intelliqittrainings/maven.git")
    }
    stage('ContBuild_Master')
    {
        cicd.newMaven()
    }
    stage('ContDeployment_Master')
    {
        cicd.newDeploy("${env.WORKSPACE}","172.31.24.16","testapp")
    }
    stage('ContTesting_Master')
    {
        cicd.newGit("https://github.com/intelliqittrainings/FunctionalTesting.git")
        cicd.runSelenium("${env.WORKSPACE}")
    }
    stage('ContDelivery_Master')
    {
        cicd.newDeploy("${env.WORKSPACE}","172.31.21.0","prodapp")
    }
    
}
