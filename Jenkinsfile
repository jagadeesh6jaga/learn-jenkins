pipeline{
    agent any

    environment {

        dockerHome = tool 'myDocker'
        mavenHome =tool 'myMaven'
        PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
    }

    stages{
        stage('checkout'){
            steps {
                sh "mvn --version"
                sh "docker version"
                echo "build"
                echo "BUILD_ID --> $env.BUILD_ID"
                echo "path --> $PATH"
                echo "BUILD NUMBER --> $env.BUILD_NUMBER"
                echo "job name --> $env.JOB_NAME"
                echo "build tag --> $env.BUILD_TAG"
                echo "build url --> $env.BUILD_URL"
            }
        }
        stage('compile'){
            steps {

                sh "mvn clean compile"
            }
        }
        // stage('integration test'){
        //     steps{
        //         sh "mvn failsafe:integration-test failsafe"
        //     }
        // }
        stage('Package'){
            steps{
                sh "mvn package -DskipTests"
            }
        }
        stage('build Docker Image'){
            steps{

                // "docker build -t 6226/currencyexchange:$env.BUILD_TAG"
                script{
                   dockerImage =  docker.build("6226/currencyexchange:${env.BUILD_TAG}")
                }
            }
        }

        stage('push Docker Image'){
            steps{
                script{
                    docker.withRegistry('', 'dockerHub'){
                    dockerImage.push();
                    dockerImage.push('latest');
                    }

                }
            }
        }
    }





}