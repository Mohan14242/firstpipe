pipeline {
    agent any

    stages {
        stage('Read File') {
            steps {
                script {
                    def fileContent = readFile('package.json')
                    echo "File content:"
                    def content=fileContent.version
                    echo content
                }
            }
        }
    }
}
