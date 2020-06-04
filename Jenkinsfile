#!/usr/bin/env groovy
pipeline {
  agent any

  stages {
    stage('构建') {
        steps {
            echo 'Building..$(branch)'
        }
    }
    stage('测试') {
        steps {
            echo 'Testing..'
        }
    }
    stage('发布') {
        steps {
            echo 'Deploying....'
        }
    }
  }
}
