node{
 stage('Source'){
    checkout scm
 }
  def mvnHome = tool 'MAVEN_HOME'
 stage('Build'){
      bat "${mvnHome}/bin/mvn clean install" 
  }
  stage('CodeQualityCheck'){
      bat "${mvnHome}/bin/mvn clean sonar:sonar" 
  }
  stage('UploadArtifacts'){
      bat "${mvnHome}/bin/mvn clean deploy" 
  }
  stage('DeployApplication'){
    echo "Deploy the application in tomcat" 
  }
 stage('Run Selenium Test'){
    echo "run selenium tests using testNG"
  }
  stage('Performane Tests'){
    echo "run load testing using jmeete tool"
   }
 
}
