node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'Sonar-scanner';
    withSonarQubeEnv() {
      bat "${scannerHome}\\bin\\sonar-scanner.bat"
    }
  }
}
