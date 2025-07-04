node {
  stage('SCM') {
    checkout scm
  }
  stage('Build') {
    sh './gradlew build'
  }
  stage('SonarQube Analysis') {
    withSonarQubeEnv('SonarQube') {
      sh 'sonar-scanner'
    }
  }
}

