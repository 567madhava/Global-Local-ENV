pipeline {

    agent any
    environment {
        DEMO_NUMBER = 'DEMO-1.1'
        //build_for = 'PROD'
        remote_server = '1.1.1.1'
        remote = '2.2.2.2'
    }

    stages {

        stage("Env Variables") {
            steps {
                //sh "printenv"
                echo "${env.JAVA_HOME}"
                echo "$JAVA_HOME"
                
                echo "${env.mvn}"
                echo "$mvn"
                
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
                //sh "printenv"
                sh 'echo "HI"'
            }
        }
    }
}
