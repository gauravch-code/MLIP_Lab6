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
                echo "Test Step: We run testing tool like pytest here"

                rem Example if using Miniconda:
                rem "C:\\Users\\YourName\\miniconda3\\Scripts\\conda.exe" run -n mlip pytest

                echo "pytest not run"
                exit 1  rem Remove or comment out this line once you add the real pytest command
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
