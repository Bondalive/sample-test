pipeline { 
agent any
stages {
stage('clean') {
steps{
echo 'cleaning..'
bat 'mvn clean'
}
}
stage('Package') {
steps {
echo 'Testing..'
bat 'mvn package'
}
}
stage('Deploy') {
steps {
echo 'Deploying....'
deploy adapters: [tomcat8(credentialsId: 'tomcat_credentials', path: '', url: 'http://localhost:9999/')], contextPath: null, war: '**/*.war'
}
}
}
}
