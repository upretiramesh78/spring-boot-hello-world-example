node{
stage('SCM Checkout'){
git 'https://github.com/upretiramesh78/spring-boot-hello-world-example'
}
stage('compile-package') {
 sh 'echo $PATH'
 def mvnHome= tool name: 'mavenNw', type: 'maven'
 sh "${mvnHome}/bin/mvn -s /usr/local/apache-maven-3.5.4/conf/settings.xml install"
}
   stage ('Server Stop and start'){
    sh "/Users/rameshchandra/Downloads/apache_tomcat/bin/shutdown.sh"
    sh "/Users/rameshchandra/Downloads/apache_tomcat/bin/./catalina.sh run"
    sleep(time:60,unit:"SECONDS")  
  }
}
