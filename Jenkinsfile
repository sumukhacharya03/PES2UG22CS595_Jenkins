pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o PES2UG22CS595-1 main.cpp'  // Compiling the C++ file
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh './PES2UG22CS595-1'  // Running the compiled executable
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
