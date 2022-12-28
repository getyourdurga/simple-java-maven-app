pipeline{
    agent any{
        stage('checkout stage'){
            steps{
                script{
                    checkout([$class: 'GitSCM', branches: [[name: 'pipeline_testing']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/getyourdurga/simple-java-maven-app.git']]])
                }
            }
        }
    }
}
    