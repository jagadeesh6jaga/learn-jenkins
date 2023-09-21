pipeline {
    agent { node { label 'workstation-node'}}
    environment {
                SERVICE_CREDS = "SERVICE CREDENTIAL ARE EMPTY"
                credentials_of_ssh = CREDENTIAL('centos-ssh')
            }

    stages {
        stage('Hello') {
            steps {
                echo 'Hello'
            }
        }
        stage('Hello world'){
            steps{
                echo 'Hello World'
                echo SERVICE_CREDS
                echo credentials_of_ssh
            }
        }
        stage('Hello Jenkins'){
            steps{
                echo 'Hello Jenkins'
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
    }
}
