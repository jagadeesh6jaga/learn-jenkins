// declarative pipeline

pipeline{
    agent any

    // agent {
    //     docker {
    //          image 'maven:3.9.6'
    //             }
    //     }
    stages{
        stage('build'){
            steps {
                echo 'build'
                echo "BUILD_ID --> $env.BUILD_ID"
                echo "$PATH"
                echo "BUILD NUMBER --> $env.BUILD_NUMBER"
                echo "$env.JOB_NAME"
                echo "$env.BUILD_TAG"
                echo "$env.BUILD_URL"
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
