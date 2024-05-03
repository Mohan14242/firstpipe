pipeline {
    agent any
  
    stages {
        stage('Read JSON (Recommended)') {
            steps {
                script {
                    // Parse the content of the file directly as JSON
                    def jsonData = readJSON file: 'package.json'

                    // Access the 'version' field from the parsed JSON map
                    version = jsonData.version

                    echo "Version: ${version}" // Debugging statement
                }
            }
        }
        stage("Printing the Version") {
            steps {
                script {
                    echo "The version is: ${version}"
                }
            }
        }

        stage("running the dowstream job"){
            steps{
                script{
                    build job: "pipeline2" , wait:true
                }
            }
        }
        // Add other pipeline stages here...
    }
}
