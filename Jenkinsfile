pipeline {
    agent any

    triggers {
        pollSCM('H/1 * * * *')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing the project...'
                sh 'test -f hello.py'
                echo 'Python file found'
            }
        }

        stage('Success') {
            steps {
                echo 'Jenkins CI Pipeline completed successfully!'
            }
        }
    }
}
