pipeline{

  agent {
    label 'DevServer'
  }

  tools {
   maven 'myMaven'
  }
  stages{

    stage('build'){
      steps{
        sh 'mvn clean package'
      }
      post {
        success {
          archiveArtifacts artifacts: '**/target/*.war'
      }
  }
    }

    stage('test'){
      steps{
        echo "This is test stage ........."
      }
    }

    stage('deploy'){
      steps{
        echo "This is deploy stage ........."
      }
    }

  }
}