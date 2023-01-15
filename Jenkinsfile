pipeline{
  agent any
  tools {
      maven "maven3.8.6"
}     
  stages {
    stage('1GetCode'){
        steps{
            sh "echo 'cloning the latest application version' "
            git branch: 'master', credentialsId: 'GitHubCredentials', url: 'https://github.com/parocoy/maven-web-application'
        }
    }
    stage('2Test+Build'){
        steps{
           sh "echo 'running JUnit-test-cases' "
           sh "echo 'testing must passed to create artifacts' "
           sh "mvn clean package"
        }
    }
    /*
    stage('4CodeQuality'){
        steps{    
           sh "echo 'performing CodeQualityAnalysis' "
           sh "mvn sonar:sonar"
        }
    }
    stage('5uploadNexus'){
        steps{
            sh "mvn deploy"
        }
    }
    stage('6deploy2prod'){
        steps{
            deploy adapters: [tomcat9(credentialsId: 'TomcatJadCredentials', path: '', url: 'http://3.136.233.125:8081/')], contextPath: null, war: 'target/*war'
        }
    }
}
  post{
   always{
    emailext body: '''Hey guys
Please check build status.

Thanks
Landmark
+1 773 406 3199''', recipientProviders: [buildUser(), developers()], subject: 'success', to: 'paypal-team@gmail.com'
   }
   success{
    emailext body: '''Hey guys
Good job build and deployment is successful.

Thanks
Landmark
+1 773 406 3199''', recipientProviders: [buildUser(), developers()], subject: 'success', to: 'paypal-team@gmail.com'}
   failure{
    emailext body: '''Hey guys
Build failed. Please resolve issues.

Thanks
Landmark
+1 773 406 3199''', recipientProviders: [buildUser(), developers()], subject: 'success', to: 'paypal-team@gmail.com'}
     }
  */   
 }
 }   
