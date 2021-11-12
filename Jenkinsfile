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

    stage('image_build') {
      steps {
        sh 'docker build -t mycontainer .'
        echo 'Image build'
      }
    }

    stage('Image_push') {
      steps {
        sh 'docker login -u arun1801docker -p Arun@9876'
        sh 'docker tag arun1801docker/mycontainer'
        sh 'docker push mycontainer:1 arun1801docker/mycontainer:1'
        echo 'mycontainer image pushed to Dockerhub'
      }
    }

  }
}