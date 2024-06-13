pipeline {
  agent any
  stages {
    stage ('Debug') {
      steps {
        sh 'date'
        sh 'cat /etc/os-release'
        sh 'free'
      }
    }
    stage ('Build') {
      steps {
        sh 'java --version'
        echo 'Running build automation'
        sh './gradlew build --no-daemon'
        archiveArtifacts artifacts: 'dist/trainSchedule.zip'
      }
    }
  }
}
