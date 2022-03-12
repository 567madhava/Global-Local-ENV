pipeline {

    agent any
    environment {
        DEMO_NUMBER = 'DEMO-1.1'
        //build_for = 'PROD'
        remote_server = '10.10.10.10'
    }

    stages {

        stage("Env Variables") {
            steps {
                sh "printenv"
            }
        }

        stage('Reading environment variable defined in groovy file') {
            steps {
                script {
                    load "./env.groovy"
                    echo "${env.var1}"
                    echo "${env.var2}"
                    echo "${env.build_for}"
                    echo "${env.remote_server}"
                    echo "$remote_server"
                    
                }
            }
        }

        stage("Env Variables print") {
            steps {
                sh "printenv"
            }
        }
    }
}
