pipeline {
  agent any
  stages {
    stage ('Build') {
      steps {
        echo 'Java version'
        sh 'java --version'
        echo 'Gradle version'
        sh 'gradle --version'
        echo 'Running build automation'
        sh './gradlew build --no-daemon'
        archiveArtifacts artifacts: 'dist/trainSchedule.zip'
      }
    }
  }
}
