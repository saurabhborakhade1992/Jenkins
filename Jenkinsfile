pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/saurabhborakhade1992/Jenkins.git', branch: 'main')
        echo 'Repo pulled to local'
      }
    }

    stage('Build') {
      steps {
        echo 'Build success'
      }
    }

    stage('Test') {
      steps {
        bat(script: 'bat script: \'HelloWorld.bat\', returnStatus: true', returnStatus: true)
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deployment Sucessful'
      }
    }

  }
}