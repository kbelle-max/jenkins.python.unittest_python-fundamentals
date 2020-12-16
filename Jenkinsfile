pipeline {
    agent docker 
         { dockerfile true
            label 'docker'
          }
    stages {
        stage('Test') {
            steps {
                sh 'python3 -m unittest discover -s ./src/test/ -p '*_test.py''
            }
        }
    }
}
