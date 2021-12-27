node{
  
  stage('code build'){
    git 'https://github.com/Monisha0118/hotel-sample.git'
  }
  stage('build') {
    def mvnHome = tool name: 'maven3', type: 'maven'
    sh "${mvnHome}/mvn clean install"
  }
  stage('deploy to tomcat') {
    sh "cp -r /var/lib/jenkins/workspace/Hotel-web/target/hotel.war /opt/tomcat/webapps/"
   }
 }
