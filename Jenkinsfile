// Declarative //
pipeline {
agent none
stages {
stage('Build') {
agent any
steps {
checkout scm
sh 'make'
stash includes: '**/target/*.jar', name: 'app' ①
}
}
stage('Test on Linux') {
agent { ②
label 'linux'
}
steps {
unstash 'app' ③
sh 'make check'
}
post {
always {
junit '**/target/*.xml'
}
}
}
stage('Test on Windows') {
agent {
label 'windows'
}
steps {
unstash 'app'
bat 'make check' ④
}
post {
always {
junit '**/target/*.xml'
}
}
}
}
}
