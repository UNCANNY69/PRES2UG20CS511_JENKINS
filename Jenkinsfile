pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o YOUR_SRN-1 YOUR_SRN-1.cpp'
            }
        }
        stage('Test') {
            steps {
                sh './YOUR_SRN-1'
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
