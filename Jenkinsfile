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
stage('Success') {
  steps {
  echo 'success'
      emailext body: 'hello', subject: 'Hello', to: 'vish.sira@gmail.com'
    }
  }
}
}
}
}
