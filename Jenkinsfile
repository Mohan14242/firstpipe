pipeline {
    agent any

    stages {
        stage('Read JSON (Recommended)') {
            steps {
                script {
                    // Read the content of the file and parse it as JSON
                    def jsonData = readFile('package.json')

                    echo jsonData["version"]
                    
                    // Access data from the parsed JSON map
                    
                }
            }
        }
        // Add other pipeline stages here...
    }
}
