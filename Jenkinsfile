pipeline {
	agent any
	stages {
		stage("build") {
			steps {
				echo 'building the applicaiton...'
			}
		}
		stage("test") {
			steps {
				echo 'testing the applicaiton...'
			}
		}
		stage("deploy") {
			steps {
				echo 'deploying the applicaiton...'
			}
		}
	}
}
<<<<<<< HEAD:jenkinsfile

pipeline {
	agent any
	stages {
		stage("build") {
			steps {
				echo 'building the applicaiton...'
			}
		}
		stage("test") {
			steps {
				echo 'testing the applicaiton...'
			}
		}
		stage("deploy") {
			steps {
                echo "${env.GIT_BRANCH}"
				echo 'deploying the applicaiton...'
			}
		}
	}
    post {
            always {
                echo 'building..'
            }
            success {
                echo 'success'
            }
            failure {
                echo 'failure'
            }
        }
    }
=======
>>>>>>> f947260e2444d8ef410b316476f1c4bc4794e051:Jenkinsfile
