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
def username = 'Jenkins'
echo 'Hello Mr. ${username}'
echo "I said, Hello Mr. ${username}"
  
}
}
stage('Deploy') {
steps {
echo 'Deploying....'
}
}
}
}
