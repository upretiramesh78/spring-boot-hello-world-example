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
    sh "cp /Users/Shared/Jenkins/Home/workspace/testpipeline/target/spring-boot-hello-world-example-0.0.1-SNAPSHOT.jar  /Users/rameshchandra/Downloads/apache_tomcat/custom/webapps/"
    sleep(time:60,unit:"SECONDS")  
  }
}
