node {
    stage('download code from SCM') {
    git branch: 'test', url: 'https://github.com/Darshana1616/Project.git'
                                    }
    stage('convert into artifacts') {
    sh 'mvn package'
                                    }
    stage('deployment') {
    deploy adapters: [tomcat9(credentialsId: '84cd2ee8-fc7f-4764-b33a-cd33d9b45a35', path: '', url: 'http://16.171.35.172:8080')], contextPath: '/Project', war: '**/*.war'
}
}
