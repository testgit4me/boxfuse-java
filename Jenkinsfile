def gv
pipeline {

    agent any
    
    tools{
        maven "maven3"
    }

    stages {
        
        stage("init"){
            steps{
                script {
                    gv = load "script.groovy"                
            }
        }

        stage("building jar"){
            steps{
                script(){
                    gv.buildJar()
                }                
            }
        }
        
        stage("building image"){
            steps{
                script(){
                    gv.buildImage()
                }              
            }
        }

        stage("Pushing image"){
            steps{
                script(){
                    gr.pushImage()
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