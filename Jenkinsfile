pipeline {
  agent {
    docker {
      image 'urand0m/squidtor:latest'
      args '--rm -h squidtor -p 3400:3400'
    }
    
  }
  stages {
    stage('Build') {
      steps {
        sh 'hostname && ip addr show'
        sh 'id'
      }
    }
    stage('Run Security Scan') {
      steps {
        sh '/usr/bin/python /home/urandom/nessrest.py'
      }
    }
  }
}