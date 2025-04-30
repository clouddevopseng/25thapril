node {
    stage('Download the code') {
    git branch: 'dev', url: 'https://github.com/clouddevopseng/25thapril.git'
     }
     stage('Build Artifacts') {
     sh 'mvn package'
     }
     stage('Deployment') {
     deploy adapters: [tomcat9(credentialsId: 'dev', path: '', url: 'http://13.203.86.11:8080')], contextPath: '/dev-config', war: '**/*.war' 
     }
}
