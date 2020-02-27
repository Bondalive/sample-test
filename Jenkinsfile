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
bat 'mvn tomcat7:deploy'
}
}
}
}
