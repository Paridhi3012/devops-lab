node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'sonar-scanner';
    withSonarQubeEnv() {
      bat "${scannerHome}\\bin\\sonar-scanner.bat"
    }
  }
}
