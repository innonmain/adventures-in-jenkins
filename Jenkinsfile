@Library('lexmarkweb-jenkins-library') _

pipeline {
  agent { label 'linux'}
  stages {
    stage('adventure') {
      steps {
        echo "The branch name is $BRANCH_NAME"
        helloWorld name:'Penelope'
      }
    }
    stage('build') {
      when {
        expression { return env.BRANCH_NAME ==~ /^release-/ }
      }
      steps {
        echo "This is a release build."
      }
    }
  }
}
