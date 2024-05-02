pipeline {
    agent any

    stages {
        stage('Read JSON (Recommended)') {
            steps {
                script {
                    // Read the content of the file as a string
                    def fileContent = readFile('package.json')

                    // Parse the string content as JSON
                    def jsonData = readJSON text: fileContent

                    // Access the 'version' field from the parsed JSON map
                    def version = jsonData.version
                    echo "Version: ${version}"
                }
            }
        }
        // Add other pipeline stages here...
    }
}
