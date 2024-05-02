pipeline {
    agent any

    stages {
        stage('Read Version') {
            steps {
                script {
                    def packageJson = readJSON file: 'package.json'
                    def version = packageJson.version
                    echo "Version: ${version}"
                }
            }
        }
    }
}
