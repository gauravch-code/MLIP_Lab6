pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat '''
                echo "In C or Java, we can compile our program in this step"
                echo "In Python, we can build our package here or skip this step"
                '''
            }
        }
        stage('Test') {
            steps {
                bat '''
                echo "Running tests using the existing virtual environment"
                "C:\\Users\\gaura\\mlip\\Scripts\\python.exe" -m pytest
                '''
            }
        }
        stage('Deploy') {
            steps {
                echo "In this step, we deploy our project"
            }
        }
    }
}
