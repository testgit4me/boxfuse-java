pipeline {

    agent any

    stages {

        stage("build"){

            when{
                expression {
                    BRANCH_NAME == 'dev' && CODE_CHANGES == true
                }
            }

            steps{
                echo "building the application..."
            }
        }

        stage("test"){
            steps {
                echo "testing the application"
            }
        }

        stage("deploy"){
            steps{
                echo "deploying the application"
            }
        }

        stage("prod"){
            steps{
                echo("prod the application...")
            }
        }
    }
}