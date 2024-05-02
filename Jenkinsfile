pipeline {
    agent any

    stages {
        stage('Read JSON (Recommended)') {
            steps {
                script {
                    // Read the content of the file as a string
                    def fileContent = readFile('package.json')

                    // Parse the string content as JSON
                   echo fileContent["version"]
                }
            }
        }
        // Add other pipeline stages here...
    }
}
