pipeline{
    agent any
    stages{
        stage('checkout'){
            steps{
                git 'https://github.com/Akila-Ayanthi/Project_02'
            }
        }
        stage('build'){
            steps{
                sh './build.sh'
            }
        }
        stage('test'){
            steps{
                sh './test.sh'
                }
        }
	stage('deploy'){
            steps{
                sh './deploy.sh'
            }
        }
    }
    post{
        always{
            echo "This will run always"
        }
        failure{
            echo "This will run only if failed"
        }
        success{
            echo "This will run only if successful"
        }
    }
}