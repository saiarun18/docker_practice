pipeline {
  agent any
  stages {
    stage('Dev_Download') {
      steps {
        git 'https://github.com/saiarun18/devops_projectpractice.git'
      }
    }

    stage('MVN_Build') {
      steps {
        sh 'mvn clean install'
      }
    }

  }
}