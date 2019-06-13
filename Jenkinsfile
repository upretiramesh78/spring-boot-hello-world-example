
env.user = 'rameshchandra'

env.host = "localhost"
env.port = "8081"

env.SRC_DIR = '/Users/Shared/Jenkins/Home/workspace/testpipeline/'
env.DEST_DIR = '/Users/rameshchandra/Downloads/apache_tomcat/'


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
    
   sh 'echo Success'
  }
}
