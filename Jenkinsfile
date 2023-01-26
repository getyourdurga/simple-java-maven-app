pipeline{
    agent any 
    tools{
        maven 'maven 3.8'
    }

    stages{
            stage('Buildstage'){
                steps{
                    script{
                        echo "Code build"
                        sh 'mvn clean install'
                    }
                }
            }
            
        
        stage('Teststage'){
            steps{
                script{
                    echo "Testing"
                    sh 'mvn test'
                }
            }
        }
        
        stage('sonar'){
            steps{
                script{
                    //def scannerHome = tool name: 'mySonarScanner';
                    withSonarQubeEnv("mysonarqube") {
                        sh "${tool("mysonarqube")}/bin/sonar-scanner \
                        -Dsonar.projectKey=simple-java-maven-app \
                        -Dsonar.sources=. \
                        -Dsonar.java.binaries=target \
                        -Dsonar.host.url=http://172.31.2.241:9000 \
                        -Dsonar.login=sqp_8bd7b9b64d9dc54338e8a12fd2794d160787d72e"
                    }
                }
            }
        }      

        stage('upload artifact to nexus '){
        steps{
            script{
                sh 'mvn -s settings.xml deploy'
            }
        }
        }
    }     
            
}





        
                    
                    
            
        
    