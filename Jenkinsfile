pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        sh './mvnw clean compile'
      }
    }

    stage('Static Analysis') {
      steps {
        sh '''mvn clean verify sonar:sonar \\
  -Dsonar.projectKey=Petclinic \\
  -Dsonar.projectName=\'Petclinic\' \\
  -Dsonar.host.url=http://13.49.77.159:9000 \\
  -Dsonar.token=sqp_a9a7fd85cb5a8907ce05662cf9935fd8c5394f24'''
      }
    }

  }
}