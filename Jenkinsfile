#! groovy
node{
 stage('Source'){
     git 'https://github.com/madhav517/myweb.git'
 }
 
 stage('Build'){
    // def mvnHome = tool 'maven3'
    sh "/home/aws/devops/maven350/bin/mvn clean package" 
 }
 stage('Send Email'){
     mail bcc: '', body: 'Demo Pipeline', cc: '', from: '', replyTo: '', subject: 'Pipeline Demo', to: 'madhav517@gmail.com'
 }
 stage('Archive'){
     archiveArtifacts 'target/*.war'
 }
}
