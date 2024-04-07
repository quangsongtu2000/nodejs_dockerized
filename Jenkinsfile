pipeline{
  agent any
  tools {
        nodejs 'nodejs' // Đặt tên tool Node.js bạn đã cấu hình trong Jenkins
  }
  stages {
    stage("checkout"){
      steps{
        checkout scm
      }
    }

    stage("Test"){
      steps{
        // sh 'sudo apt-get install npm'
        sh 'npm test'
      }
    }

    stage("Build"){
      steps{
        sh 'npm run build'
      }
    }
  }
}
