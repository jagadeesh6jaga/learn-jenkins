// declarative pipeline

pipeline{
    // agent any
    agent {
        docker {
            image 'maven:3.9.6'
            }
        }
    stages{
        stage('build'){
            steps {
                echo 'build'
            }
        }
        stage('test'){
            steps{
                echo 'test'
            }
        }
        stage('deploy'){
            steps{
                echo 'deploy'
            }
        }

    }
    post{
        always {
            echo "i run always"
        }
        success {
            echo "i run when pipeline success"
        }
        failure {
            echo "i run when pipeline failed"
        }
    }
        
        
        
}
