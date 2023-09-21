pipeline {
    agent { node { label 'workstation-node'}}
    // triggers{
    //     cron('*/1 * * * *')
    // }
    environment {
                SERVICE_CREDS = "SERVICE CREDENTIAL ARE EMPTY"
                credentials_of_ssh = credentials('centos-ssh')
                branch  = 'prod'
            }
    // parameters {
    //     string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

    //     text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

    //     booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

    //     choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

    //     password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    // }
    
    stages {
        stage('Hello') {
            when {
                branch 'prod'
            }
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
            // input {
            //     message "Should we continue?"
            //     ok "Yes, we should."
            //     submitter "alice,bob"
            //     parameters {
            //         string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
            //     }
            // }
            steps{
                echo 'Hello Jenkins'
            }
        }
    //     stage('parameters of input'){
    //         steps{
    //             echo "Hello ${params.PERSON}"

    //             echo "Biography: ${params.BIOGRAPHY}"

    //             echo "Toggle: ${params.TOGGLE}"

    //             echo "Choice: ${params.CHOICE}"

    //             echo "Password: ${params.PASSWORD}"
    //     }
    // }
    // }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
    }
}
}