parameters {
string(name: 'Greeting', defaultValue: 'Hello', description: 'How should I
greet the world?')
}
       
       
pipeline {
agent any
stages {
stage('Build') {
steps {
echo 'Building..'
}
}
stage('Test') {
steps {
echo 'Testing..'
echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}" 
 echo "${params.Greeting} World!"
}
}
stage('Deploy') {
steps {
echo 'Deploying....'
}
}
}
}
