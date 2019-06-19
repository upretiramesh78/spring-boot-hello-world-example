
env.user = 'rameshchandra'

env.host = "localhost"
env.port = "8081"

env.SRC_DIR = '/Users/Shared/Jenkins/Home/workspace/testpipeline/'
env.DEST_DIR = '/Users/rameshchandra/Downloads/apache_tomcat/'



env.sourFile=$SRC_DIR/spring-boot-hello-world-example-0.0.1-SNAPSHOT.jar
env.destFile=$DEST_DIR/spring-boot-hello-world-example-0.0.1-SNAPSHOT.jar




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
    chmod 777 $DEST_DIR
    echo "Copying files from $sourFile"
    
   cp $SRC_DIR $DEST_DIR

    echo "Copying files from $sourConfigFolder"
    cp -r $SRC_DIR $DEST_DIR
    #nohup nice java -jar $destFile --server.port=$port $properties $> $dstLogFile 2>&1 &

   
   sh 'echo Success'
  }
}
