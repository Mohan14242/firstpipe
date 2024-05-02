pipeline {
    agent any

    stages {
        stage('Read JSON (Recommended)') {
            steps {
                script {
                    // Read the content of the file and parse it as JSON
                    def jsonData = readJSON file: 'package.json'
                    
                    // Access data from the parsed JSON map
                    def version = jsonData.version
                    echo "Version: ${version}"
                }
            }
        }
        // Add other pipeline stages here...
    }
}
