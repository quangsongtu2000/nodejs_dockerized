pipeline{
  agent any
  stages {
    stage("checkout"){
      steps{
        checkout scm
      }
    }

    stage("Test"){
      steps{
        sh 'sudo apt-get install npm'
        sh 'npm test'
      }
    }

    stage("Build"){
      steps{
        sh 'npm run build'
      }
    }

    stage("Build Images"){
      steps{
        sh 'docker build -t my-apps .'
      }
    }
  }
}
