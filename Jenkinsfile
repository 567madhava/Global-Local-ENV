pipeline { 
  
	agent any
	
	environment {
		BUILD_ON = "PROD"
		SKYPE_TEST_CASES = "TRUE"
		REMOTE_SERVERS = '0.0.0.10'
		MAVEN_VERSION = '2.0.0'
    }

	stages {
		stage("1-Env Variables") {
            steps {
                sh "printenv"
            }
		}
        stage('stage-1') {
            steps {
                echo "This is first demo piple $BUILD_NUMBER"
            }
        }
		stage('Reading environment variable defined in groovy file') {
			environment {
                // environment variables would be initialized in the script file
                LS = "${sh(script: 'chmod +x ./env_values.sh; ./env_values.sh', returnStdout: true).trim()}"
            }
		}
        stage("2-Env Variables") {
            steps {
                sh "printenv"
            }
        }
    }
}
