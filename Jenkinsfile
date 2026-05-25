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
stage('Deploy Container') {
steps {
sh 'docker rm -f frontenddeployment || true'
sh 'docker run -d -p 3000:3000 --name frontenddeployment frontenddeployment'
}
}
}
}

