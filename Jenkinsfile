pipeline {

    agent any
    environment {
        DEMO_NUMBER = 'DEMO-1.1'
        //build_for = 'PROD'
        remote_server = '1.1.1.1'
        remote = '2.2.2.2'
    }
    tools {
        //maven 'mvn3.8.4'
        maven 'mvn3.5.0'
    }

    stages {

        stage("Env Variables") {
            steps {
                //sh "printenv"
                //echo "${env.maven}"
                //echo "$maven"
                
                //echo "${env.java}"
                //echo "$java"
                sh " mvn --version "
                
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
                    echo "${env.remote}"
                    echo "$remote"
                    
                }
            }
        }

        stage("Env Variables print") {
            steps {
                echo "$remote"
                script {
                    echo "$remote"
                }
            }
        }
    }
}
