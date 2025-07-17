pipeline {
  agent any

  stages {
    stage('Clone Repo') {
      steps {
        git 'https://github.com/durgaprasad2915/CAKE_Site_Demo.git'
      }
    }

    stage('Build Docker Image') {
      steps {
        sh 'docker build -t cake-frontend ./frontend'
      }
    }

    stage('Run Container') {
      steps {
        sh 'docker run -d -p 3000:3000 --name cake-frontend cake-frontend'
      }
    }
  }
}
