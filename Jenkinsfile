env.MYTOOL_VERSION = '1.33'
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
}
}
stage('Deploy') {
steps {
echo 'Deploying....'
}
}
}
}
