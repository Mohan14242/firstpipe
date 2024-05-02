pipeline {
    agent any

    stages {
        stage('Read File') {
            steps {
                script {
                    def fileContent = readFile('package.json')
                    echo "File content:"
                    echo fileContent
                    
                }
            }
        }
    }
}
