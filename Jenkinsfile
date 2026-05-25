pipeline {
agent any
stages {
stage('Clone Code') {
steps {
git 'https://github.com/kongarashiva/frontenddeployment.git'
}
}
stage('Build Docker Image') {
steps {
sh 'docker build -t frontenddeployment .'
}
}

