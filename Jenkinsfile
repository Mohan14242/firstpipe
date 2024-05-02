pipeline {
    agent any

    stages {
        stage('Read Version') {
            steps {
                script {
                    def fileContent = readFile('package.json')
                    def json = readJSON text: fileContent
                    def version = json.version
                    echo "Version: ${version}"
                }
            }
        }
    }
}
