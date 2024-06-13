pipeline {
  agent any
  stages {
    stage ('Build') {
      steps {
        echo 'Running build automation'
        sh './gradlew build --no-daemon'
        echo 'Java version'
        sh 'java --version'
        archiveArtifacts artifacts: 'dist/trainSchedule.zip'
      }
    }
  }
}
