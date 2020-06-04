#!/usr/bin/env groovy
pipeline {
  environment{
     branch=sh(returnStdout:true,script: 'echo $branch').trim()
  }
  agent any

  stages {
    stage('构建') {
        steps {
            echo 'Building..${branch} $branch '
        }
    }
    stage('测试') {
        steps {
            echo 'Testing.. ${branch1}'
        }
    }
    stage('发布') {
        steps {
            echo 'Deploying....'
        }
    }
  }
}
