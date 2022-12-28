pipeline{
    agent any 
    tools{
        maven 'maven 3.8'
    }
    stages{
        stage('Build'){
            steps{
                script{
                    echo "Code Compile"
                    sh 'mvn compile'
                }
            }
        }
        stage('Test'){
            steps{
                script{
                    echo"Test stage"
                    sh 'mvn clean test'
                }
            }
        }
    }
}
        
    