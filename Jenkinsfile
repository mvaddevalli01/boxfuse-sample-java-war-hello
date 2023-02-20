pipeline 
{
agent any
environment {
      PATH = "/bin/mvn:$PATH"
  }
  

stages
 {
      stage("get the code from git")
	{
          steps
		{
            	git branch: 'master', url: 'https://github.com/GREATCODERHYD/boxfuse-sample-java-war-hello.git'
          
          }
      }
      


stage("build the code ")
	{
          	steps
		{
              sh "mvn clean package"
          	}
      }

stage("deploy stage")
{
          steps
		{
            	deploy adapters: [tomcat9(credentialsId: 'deploy1111', path: '', url: 'http://52.3.242.54:8080')], contextPath: 'bhupesh', war: '**/*.war'
          	}
 }
 

 }
}
