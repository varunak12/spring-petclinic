node {

 
stage('init') {

 
checkout scm

 
}

 
stage('build') {

 
sh '''

 
mvn clean package

 
'''

 
}

 
stage('Build image') {

 
app = docker.build("varunak12/petclinic")

 
}

 
 

 
stage('push image') {

 
docker.withRegistry('https://registry.hub.docker.com', 'DOCKERHUB') {

 
app.push("latest")

 
}

 
echo "trying to docker image to docker hub"

 
}

 
 

 
}
