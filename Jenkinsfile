pipeline {
agent any
stages {
stage('Test') {
steps {
sh 'make check'
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
