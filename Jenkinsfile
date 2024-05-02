pipeline {
    agent any

    stages {
        stage('Read JSON (Recommended)') {
            steps {
                script {
                    // Parse the content of the file directly as JSON
                    def jsonData = readJSON file: 'package.json'

                    // Access the 'version' field from the parsed JSON map
                    def version = jsonData.version
                    echo "Version: ${version}"
                }
            }
        }
        // Add other pipeline stages here...
    }
}
