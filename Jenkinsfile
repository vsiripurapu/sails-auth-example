pipeline {
  agent {
    docker {
      image 'ubuntu:latest'
    }

  }
  stages {
    stage('build') {
      steps {
        sh 'sh apt-get install node npm'
        git(url: 'https://github.com/vsiripurapu/sails-auth-example.git', branch: 'master', credentialsId: 'vsiripurapu')
        sh '''sh cd sail*
sh sails lift'''
      }
    }

  }
}