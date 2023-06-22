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
        stage("Build"){
            steps{
                sh "maven install"
            }
            
        }
        stage("Deploy on Test"){
            steps{
                //Deploying on test
                deploy adapters: [tomcat9(credentialsId: 'tomcatserverdetails1', path: '', url: 'http://10.1.255.128:80')], contextPath: '/app', war: '**/*.war'
            }
            
        }
        stage("Deploy on Prod"){
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
