pipeline {

    agent any
    
    tools{
        maven 'maven3'
    }

    stages {

        stage("building"){
            steps{
                echo "building the application..."
                sh "mvn package"
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