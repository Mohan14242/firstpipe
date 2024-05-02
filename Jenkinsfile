pipeline {
    agent any

    stages {
        stage('Read File') {
            steps {
                script {
                   def props = readJSON file: 'package.json'
                   echo props.version
                    
                }
            }
        }
    }
}
