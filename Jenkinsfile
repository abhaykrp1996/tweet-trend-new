pipeline
{
    agent{
        node{
            label "maven"
        }
    }
environment
    {
        path = "/opt/apache-maven-3.9.6/bin/:&PATH"
    
    stages
    {
        stage("build")
        {
            steps {
                sh 'mvn clen deploy'
            }
        }
    }
}
