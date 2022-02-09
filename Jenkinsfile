// pipeline {
// 	agent any
// 	stages {
// 		stage("build") {
// 			steps {
// 				echo 'building the applicaiton...'
// 			}
// 		}
// 		stage("test") {
// 			steps {
// 				echo 'testing the applicaiton...'
// 			}
// 		}
// 		stage("deploy") {
// 			steps {
//                 echo "${env.GIT_BRANCH}"
// 				echo 'deploying the applicaiton...'
// 			}
// 		}
// 	}
//     post {
//             always {
//                 echo 'building..'
//             }
//             success {
//                 echo 'success'
//             }
//             failure {
//                 echo 'failure'
//             }
//         }
//     }

// pipeline {
// 	agent any
// 	stages {
// 		stage("build") {
// 			when {
// 				expression {
// 					env.GIT_BRANCH == 'origin/main'
// 				}
// 			}
// 			steps {
// 				echo 'building the applicaiton...'
// 			}
// 		}
// 		stage("test") {
// 			when {
// 				expression {
// 					env.GIT_BRANCH == 'origin/test' || env.GIT_BRANCH == ''
// 				}
// 			}
// 			steps {
// 				echo 'testing the applicaiton...'
// 			}
// 		}
// 		stage("deploy") {
// 			steps {
// 				echo 'deploying the applicaiton...'
// 			}
// 		}
// 	}
// }

// pipeline {
// 	agent any
// 	environment {
// 		NEW_VERSION = '1.0.0'
// 	}
// 	stages {
// 		stage("build") {
// 			steps {
// 				echo 'building the applicaiton...'
// 				echo "building version ${NEW_VERSION}"
// 			}
// 		}
// 		stage("test") {
// 			steps {
// 				echo 'testing the applicaiton...'
// 			}
// 		}
// 		stage("deploy") {
// 			steps {
// 				echo 'deploying the applicaiton...'
// 			}
// 		}
// 	}
// }

pipeline {
	agent any
	environment {
		NEW_VERSION = '1.0.0'
		ADMIN_CREDENTIALS = credentials('admin')
	}
	stages {
		stage("build") {
			steps {
				echo 'building the applicaiton...'
				echo "building version ${NEW_VERSION}"
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
				echo "deploying with ${ADMIN_CREDENTIALS}"
				sh 'printf ${ADMIN_CREDENTIALS}'
			}
		}
	}
}