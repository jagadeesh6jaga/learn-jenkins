pipeline {
    agent { node { label 'workstation-node'}}

    stages {
        stage('Hello') {
            steps {
                echo 'Hello'
            }
        }
        stage('Hello world'){
            steps{
                echo 'Hello World'
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
