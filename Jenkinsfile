pipeline {

    agent any
    environment {
        DEMO_NUMBER = 'DEMO-1.1'
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
                    load "./pipeline/basics/extenvvariable/env.groovy"
                    echo "${env.env_var1}"
                    echo "${env.env_var2}"
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
