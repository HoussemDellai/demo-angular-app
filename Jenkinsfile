node {
  stage('Checkout SCM') {
    git branch: 'patch-3', url: 'https://github.com/subbuto/demo-angular-app.git'
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
