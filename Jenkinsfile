@Library("mylibrary")_
node('built-in')
{
    stage('ContDownloa_Loans')
    {
        cicd.newGit("https://github.com/intelliqittrainings/maven.git")
    }
    stage('ContBuild_Loans')
    {
        cicd.newMaven()
    }
    
}
