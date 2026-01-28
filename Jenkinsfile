pipeline {
  agent any

  triggers {
    cron '* * * * *'
  }

  stages{
    stage('Checkout') {
      steps {
          git 'https://github.com/abm570/flask-demo.git'
      }
    }

    stage('Building') {
       steps {
          echo 'Building from Jenkins'
      }
    }

    stage('Testing') {
        steps {
          sh 'python3 app.py'
        }
    }
  }  
}
