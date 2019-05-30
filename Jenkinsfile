node{

stage('SCM Checkout'){
git 'https://github.com/upretiramesh78/spring-boot-hello-world-example.git'
}
stage('compile-package') {
 def mvnHome= tool name: 'maven', type: 'maven'
 
 sh "${mvnHome}/bin/ mvn clean"
}
}
