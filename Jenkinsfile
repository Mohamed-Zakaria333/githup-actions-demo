// Declarative //
pipeline {
agent none
stages {
stage('Back-end') {
agent {
label 'linux'
docker { image 'maven:3-alpine' }
}
steps {
sh 'mvn --version'
}
}
stage('Front-end') {
agent {
label 'linux'  
docker { image 'node:7-alpine' }
}
steps {
sh 'node --version'
}
}
}
}
