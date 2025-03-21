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
                echo "Test Step: Creating virtual environment"
                python -m venv mlip

                echo "Activating venv and installing dependencies"
                mlip\\Scripts\\pip install --upgrade pip
                mlip\\Scripts\\pip install pytest numpy pandas scikit-learn

                echo "Running tests using venv"
                mlip\\Scripts\\python.exe -m pytest
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
