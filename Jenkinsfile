node{
  stage('SCM') { 
    git branch: 'main', credentialsId: 'thanh1072004-github', url: 'https://github.com/thanh1072004/Baitap1.git' 
  } 
  stage('SonarQube Analysis') { 
   def scannerHome = tool 'SonarQube Scanner'; 
    withSonarQubeEnv() { 
      sh "${scannerHome}/bin/sonar-scanner -Dsonar.java.binaries=.  -Dsonar.projectKey=KimMinh_TuanMinh -Dsonar.login=sqa_9aa34f5f3fe3e2b7af7151bc96e7bc4fa84ee7c9" 
    } 
  } 
}
