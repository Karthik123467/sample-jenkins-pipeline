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

        stage('Run Shell Script') {
            steps {
                bat 'script.bat'
            }
        }

        stage('Print Directory Contents') {
            steps {
                bat 'cd'
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
