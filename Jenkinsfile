pipeline {
    environment {
        // Here if you create any variable you will have global access, since it is environment no need of def
        packageVersion = ''
    }
    agent any
    stages {
        stage('Get version') {
            steps {
                script {
                    def packageJson = readJSON file: 'package.json'
                    packageVersion = packageJson.version
                    echo "Version: ${packageVersion}"
                }
            }
        }
        stage("Printing the version") {
            steps {
                script {
                    echo "The version is ${packageVersion}"
                }
            }
        }
    }
}
