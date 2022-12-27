pipeline{
    agent any {
        stages{
            stage("Checkout stage"){
                steps{
                    checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/getyourdurga/simple-java-maven-app.git']]])
                }
            }
        }
    }
}