pipeline {
 agent any
 tools {
 nodejs 'ode js 16' // Sesuaikan dengan nama Node.js yang

 }
 stages {
 stage('Checkout') {
 steps {
 git branch: 'main', url:
'https://github.com/Rofiq02bae/nodejs.git'
 }
 }
 stage('Install Dependencies') {
 steps {
 sh 'npm install'
 }
 }
 stage('Run Tests') {
 steps {
 sh 'npm test'
 }
 post {
 success {
 junit 'test-results.xml' // Sesuaikan dengan lokasifile hasil tes
 }
 failure {
 echo 'Tests failed!'
 }
 }
 }
 stage('Build') {
 steps {
 sh 'npm run build' // Sesuaikan dengan perintah build diproyek Anda
 }
 }
 stage('Deploy') {
 steps {
 echo 'Deploying to production environment...'
 // Tambahkan perintah deploy sesuai kebutuhan Anda
 }
 }
 }
 post {
 success {
 echo 'Pipeline completed successfully!'
 }
 failure {
 echo 'Pipeline failed!'
 }
 }
}
