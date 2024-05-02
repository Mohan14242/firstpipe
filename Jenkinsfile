pipeline {
    agent any

    stages {
        stage('Read File') {
            steps {
                script {
                   props = readJSON file: 'package.json'
                   echo props.version
                    
                }
            }
        }
    }
}
