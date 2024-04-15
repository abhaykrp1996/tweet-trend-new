pipeline
{
    agent{
        node{
            label "maven"
        }
    }
environment
    {
        path = "/opt/apache-maven-3.9.6/bin/:$PATH"
    }
    
    stages
    {
        stage("build")
        {
            steps {
                sh 'mvn clean deploy'
            }
        }
        stage('SonarQube analysis') {
    environment {
      scannerHome = tool 'vgalaxy-sonar-scanner'
    }
    steps{
    withSonarQubeEnv('vgalaxy-sonar-server')
        { // If you have configured more than one global server connection, you can specify its name
      sh "${scannerHome}/bin/sonar-scanner"
    }
    }
  }
    }
}

