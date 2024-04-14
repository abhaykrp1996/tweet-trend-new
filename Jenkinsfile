pipeline
{
    agent{
        node{
            label "maven"
        }
    }
    stages
    {
        stage("clone code")
        {
            steps {
                git branch:'main',url:'https://github.com/abhaykrp1996/tweet-trend-new.git'
            }
        }
    }
}
