pipeline {

    agent any
    
    tools{
        maven "maven3"
    }

    stages {

        stage("building jar"){
            steps{
                echo "building application ..."
                sh "mvn package"
            }
        }
        
        stage("building image"){
            steps{
                echo "building docker image..."
                sh "docker build -t projectvprofile/java-maven-app:jma-2.1 ."                
            }
        }

        stage("Pushing image"){
            steps{
                withCredentials([usernamePassword(credentialsId: "cred-docker-hub", passwordVariable: "PASSWORD", usernameVariable: "USERNAME")]){
                    sh "echo $PASSWORD | docker login -u $USERNAME --password-stdin"                
                    sh "docker push projectvprofile/java-maven-app:jma-2.1"        
                }
                
            }
        }        

        stage("testing"){
            steps {
                echo "testing the application"
            }
        }

        stage("deploying"){
            steps{
                echo "deploying the application"
            }
        }
    }
}