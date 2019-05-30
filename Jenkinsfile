node{

stage('SCM Checkout'){
git 'https://github.com/upretiramesh78/spring-boot-hello-world-example'
}
stage('compile-package') {
 def mvnHome= tool name: 'maven3', type: 'maven'
 sh "${mvnHome}/bin1/ mvn clean"
}
}
