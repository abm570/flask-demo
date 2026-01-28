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

    stage('Install Dependencies') {
    steps {
        sh '''
            python3 -m venv venv
            . venv/bin/activate
            pip install --upgrade pip
            pip install flask
        '''
    }
}

    
    stage('Building') {
       steps {
          echo 'Building from Jenkins'
      }
    }

    stage('Testing') {
        steps {
          sh 'venv/bin/python3 app.py'
        }
    }
  }  
}
