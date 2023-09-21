pipeline {
    agent none

    stages {
        agent { node { label 'workstation-node'}}
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
}
