#!/usr/bin/env groovy
pipeline {
  environment {
     BRANCH = sh(returnStdout:true,script: 'echo $branch').trim()
  } 
  agent { docker 'php' }

  stages {
    stage('构建') {
        steps {
            sh "echo 'Buliding $BRANCH'"
        }
    }
    stage('测试') {
        steps {
            echo 'Testing..'
            sh "composer --version"
        }
    }
    stage('发布') {
        steps {
            echo 'Deploying....'
        }
    }
  }
}
