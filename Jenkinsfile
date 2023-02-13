pipeline {

    agent any
    
    tools{
        maven "maven3"
    }

    stages {

        stage("building"){
            steps{
                echo "building the application..."
                sh "mvn package"
                sh "docker build -t projectvprofile/java-maven-app:jma-2.1 ."
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