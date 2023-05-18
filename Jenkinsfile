pipeline {
agent any
stages {
stage('Test') {
steps {
echo "hello world"
}
}
}
post {
always {
junit '**/target/*.xml'
}
failure {
mail to: zx30cv31bn@gmail.com, subject: 'The Pipeline failed :('
}
}
}
