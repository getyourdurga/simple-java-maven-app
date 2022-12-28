pipeline{
    agent any 
    tools{
        maven 'maven 3.8'
    }
    stages{
        stage('Build stage'){
            steps{
                script{
                    echo "Code build"
                    sh 'mvn clean install'
                }
            }
        }
        
    }
}
        
    