pipeline {
    agent any

    stages {
        
        stage('Read JSON (Recommended)') {
            steps {
                def jsonData = readJSON file: 'package.json'
                // Access data from map
                println "Environment: ${jsonData['name']}"
            
            }
        }
        // Add other pipeline stages here...
    }
}
