#!/usr/bin/env groovy
pipeline {
  environment {
     BRANCH = sh(returnStdout:true,script: 'echo $branch').trim()
  } 
  agent any

  stages {
    stage('构建') {
        steps {
            sh "Buliding $BRANCH"
        }
    }
    stage('测试') {
        steps {
            echo 'Testing..'
            container('composer') {
            	sh "echo composer update -vvv"
            }
        }
    }
    stage('发布') {
        steps {
            echo 'Deploying....'
        }
    }
  }
}
