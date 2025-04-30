pipeline {
    agent any

    environment {
        PROJECT_NAME = 'MyJenkinsProject'
        AUTHOR = 'Kumpatlapavankumar'
    }

    stages {
        stage('Clone Repository') {
            steps {
                git url: 'https://github.com/Karthik123467/sample-jenkins-pipeline.git', branch: 'main'
            }
        }

        stage('Run Shell Scripts in Parallel') {
            parallel {
                stage('Run Script 1') {
                    steps {
                        bat 'script1.bat'
                    }
                }
                stage('Run Script 2') {
                    steps {
                        bat 'script2.bat'
                    }
                }
            }
        }

        stage('Print Directory Contents') {
            steps {
                bat 'dir'
            }
        }

        stage('Print Environment Variables') {
            steps {
                bat '''
                    echo Project: %PROJECT_NAME%
                    echo Author: %AUTHOR%
                    set
                '''
            }
        }
    }
}
