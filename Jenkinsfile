pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''#!/bin/bash
                echo 'In C or Java, we can compile our program in this step'
                echo 'In Python, we can build our package here or skip this step'
                '''
            }
        }
        stage('Test') {
            steps {
                sh '''#!/bin/bash
                echo 'Test Step: We run testing tool like pytest here'

                # TODO fill out the path to conda here
                # sudo /PATH/TO/CONDA init

                # TODO Complete the command to run pytest
                # sudo /PATH/TO/CONDA run -n <Envinronment Name> <Command you want to run>

                # Activate the virtual environment
                python3 -m venv mlip
                source mlip/bin/activate
                pip install pytest
                pip install numpy
                pip install pandas
                pip install scikit-learn

                # Run pytest
                pytest

                # Deactivate the virtual environment
                deactivate

                echo 'pytest not runned'
                # exit 1 #comment this line after implementing Jenkinsfile
                '''

            }
        }
        stage('Deploy') {
            steps {
                echo 'In this step, we deploy our porject'
                echo 'Depending on the context, we may publish the project artifact or upload pickle files'
            }
        }
    }
}
