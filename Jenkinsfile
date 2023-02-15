pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES2UG20CS511-1 PES2UG20CS511.cpp'
            }
        }
        stage('Test') {
            steps {
                sh './PES2UG20CS511-1'
            }
        }
    }
    post {
        always {
            script {
                if (currentBuild.result == 'FAILURE') {
                    echo 'pipeline failed'
                }
            }
        }
    }
}
