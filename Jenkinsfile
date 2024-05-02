pipeline {
    agent any

    stages {
        stage('Read File') {
            steps {
                script {
                    def fileContent = readFile('example.txt')
                    echo "File content:"
                    echo fileContent
                }
            }
        }
    }
}
