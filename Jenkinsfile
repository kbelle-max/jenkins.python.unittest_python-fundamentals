  
timestamps {
    node () {
        stage ('Python-test - Checkout') {
         checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '', url: 'https://github.com/kbelle-max/jenkins.python.unittest_python-fundamentals']]])
        }
        stage ('Python-test - Build') {
            sh "python -m unittest discover -s ./src/test/ -p '*_test.py'"
        }
    }
}
