pipeline {
  agent any

  stages {
    stage('Run Node Container') {
      steps {
        sh '''
          docker run --rm --name Fatima-Tul-Zahra-node node:14 bash -c "node -v && echo Node-14.1 Fatima-Tul-Zahra"
        '''
      }
    }

    stage('Run Maven Container') {
      steps {
        sh '''
          docker run --rm --name Fatima-Tul-Zahra-maven maven:3.8.6-openjdk-11 bash -c "mvn -v && echo Maven-3.8 Fatima-Tul-Zahra"
        '''
      }
    }

    stage('Verify Containers (optional)') {
      steps {
        sh 'docker ps -a || true'
      }
    }
  }
}

