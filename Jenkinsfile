node {
  stage('Checkout SCM') {
    git branch: 'main', url: 'https://github.com/subbuto/hello-world-2.git'
  }
  stage('Install node modules') {
    sh "npm install"
  }
  stage('test') {
    sh "npm run test-headless"
  }
  stage('Build') {
    sh "npm run build --prod"
  }
  stage('Copy') {
    sh "cp -a /var/lib/jenkins/angular pipeline/dist/demo-angular-app/. /var/www/demo-angular-app/html"
  }
}
