pipeline {
  agent any
  tools { 
        maven 'Maven_3_2_5'  
    }
   stages{
    stage('CompileandRunSonarAnalysis') {
            steps {	
		sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=asghenrywebapp -Dsonar.organization=asghenrywebapp -Dsonar.host.url=https://sonarcloud.io -Dsonar.token=6859f248e1ceb034f08304b68c33c22d8662da78'
			}
        } 
  }
}
