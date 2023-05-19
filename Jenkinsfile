// Declarative //
pipeline {
agent none
stages {
stage('Build') {
agent any
steps {
checkout scm
echo 'im any agent'
}
}
stage('Test on Linux') {
agent { 
label 'linux'
}
steps {
echo 'i run on linux agent'
}
post {
always {

}
}
}
stage('Test on Windows') {
agent {
label 'windows'
}
steps {
echo 'im run on windows agent'
}
post {
always {

}
}
}
}
}
