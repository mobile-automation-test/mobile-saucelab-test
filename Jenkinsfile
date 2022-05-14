node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def mvn = tool 'MavenTools';
    withSonarQubeEnv() {
      sh "${mvn}/bin/mvn clean verify sonar:sonar -Dsonar.projectKey=mobile-automation-test_mobile-saucelab-test_AYDBxCzzYYRE-rqPUN7H"
    }
  }
}