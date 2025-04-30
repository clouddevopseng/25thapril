node {
    stage('Download the code') {
    git branch: 'test', url: 'https://github.com/clouddevopseng/25thapril.git'
     }
     stage('Build Artifacts') {
     sh 'mvn package'
     }
     stage('Deployment') {
     deploy adapters: [tomcat9(credentialsId: 'test', path: '', url: 'http://65.0.32.180:8080')], contextPath: '/test-config', war: '**/*.war'
     }
}
