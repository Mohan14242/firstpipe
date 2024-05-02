pipeline {
    agent any

    stages {
        stage('Read JSON File') {
            steps {
                script {
                    // Read and parse the JSON file
                    def jsonData = readJSON text: '''
                    {
                        "name": "catalogue",
                        "version": "2.0.0",
                        "description": "product catalogue REST API",
                        "main": "server.js",
                        "scripts": {
                            "test": "echo \\"Error: no test specified\\" && exit 1"
                        },
                        "author": "SteveW",
                        "license": "Apache-2.0",
                        "dependencies": {
                            "body-parser": "^1.18.1",
                            "express": "^4.15.4",
                            "mongodb": "^3.5.3",
                            "pino": "^5.10.8",
                            "express-pino-logger": "^4.0.0",
                            "pino-pretty": "^2.5.0",
                            "@instana/collector": "^1.98.1"
                        }
                    }
                    '''

                    // Access specific fields from the parsed JSON data
                    def version = jsonData.version
                    def name = jsonData.name
                    def description = jsonData.description

                    // Print the values of the fields
                    echo "Name: ${name}"
                    echo "Version: ${version}"
                    echo "Description: ${description}"
                }
            }
        }
    }
}
