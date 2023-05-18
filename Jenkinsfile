// Declarative //
pipeline {
agent any
parameters {
string(name: 'Greeting', defaultValue: 'Hello', description: 'How should I greet the world?')
}
stages {
stage('Example') {
steps {
echo "${params.Greeting} World!"
}
}
}
post {
always {
junit '**/target/*.xml'
}
failure {
mail to: zx30cv31bn@gmail.com, subject: 'The Pipeline failed '
}
}
}

