pipeline {
    agent any


    environment {
        STRING = 'Vibe check'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                git "https://github.com/jmlagunzad/GitPractice.git"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                script {
                    if(STRING == 'Vibe check')
                    {
                        echo 'Absolutelay.'
                        bat 'test.bat'
                    }
                }
            }
        }
        stage('Deploy') {
            environment {
                STRING = 'Deploying'
            }
            steps {
                echo "${STRING}...."
                bat 'tesdir/hello.bat'
            }
        }
        stage('Parrarel') {
            parallel{
                stage('Hello') {
                    steps{
                        echo 'Hello'
                    }
                }
                stage('World') {
                    steps{
                        echo 'World'
                    }
                }
            }
            
        }
    }

    post {
        always {
            echo 'naolways'
        }
        success {
            echo 'Wowie!'
        }
        failure {
            echo 'Me :('
        }
        // unstable {
        //     echo 'This will run only if the run was marked as unstable'
        // }
        // changed {
        //     echo 'This will run only if the state of the Pipeline has changed'
        //     echo 'For example, if the Pipeline was previously failing but is now successful'
        // }
    }
}
