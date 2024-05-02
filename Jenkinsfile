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
                    def name=jsonData.name 
                    def environment=jsonData.environment
                    echo "Version: ${version}"
                    echo " the name ${name}"
                    echo " the environemtn ${environment}"

                    if (environemtn == "web"){
                        println("here we are deplying to  the dev env")
                    }
                }
            }
        }
        // Add other pipeline stages here...
    }
}
