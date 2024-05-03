pipeline {
    agent any

    stages {
        stage('Read JSON (Recommended)') {
            steps {
                script {
                    // Parse the content of the file directly as JSON
                    def jsonData = readJSON file: 'package.json'

                    // Access the 'version', 'name', and 'environment' fields from the parsed JSON map
                    def version = jsonData.version
                    def name = jsonData.name
                    def environment = jsonData.environment

                    echo "Version: ${version}"
                    echo "The name: ${name}"
                    echo "The environment: ${environment}"

                    if (environment == "web") {
                        println("Deploying to the dev environment")
                    }
                }
            }
        }


        stage("printign the version"){
            steps{
                script{
                    echo $version
                }
            }
        }

        // Add other pipeline stages here...
    }
}
