pipeline {
  agent any
  stages {
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
