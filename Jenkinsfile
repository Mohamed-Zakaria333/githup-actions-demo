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
  /* `make check` returns non-zero on test failures,
* using `true` to allow the Pipeline to continue nonetheless
*/
bat 'make check || true' ①
junit '**/target/*.xml' ②
  
}
}
stage('Deploy') {
steps {
echo 'Deploying....'
}
}
}
}
