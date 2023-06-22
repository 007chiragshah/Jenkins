pipeline{
    agent any
    tools {
        maven 'Maven' 
    }
    stages{
        stage("Test"){
            steps{
                sh "mvn --version"
            }
            
        }
        stage("Run a command"){
            steps{
                sh 'pwd'
            }
            
        }
        stage("C"){
            steps{
                sh '''pwd
                    ls
                    date
                    cal'''
            }
            
        }
        stage("D"){
            steps{
                echo "========executing A========"
            }
            
        }
    }
    post{
        always{
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}
