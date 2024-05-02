pipeline {
    agent any
    environment{
        //here if you create any variable you will have global access, since it is environment no need of def
        packageVersion = ''
    }
    stages {
        stage('Get version'){
            steps{
                script{
                    def packageJson = readFile 'package.json'
                    packageVersion = packageJson.version
                    echo "version: ${packageVersion}"
                }
            }
        }
       
        stage('Unit test') {
            steps {
                echo "unit testing is done here"
            }
        }
        //sonar-scanner command expect sonar-project.properties should be available
        stage('SAST') {
            steps {
                echo "SAST Done"
                echo "package version: $packageVersion"
            }
        }
        //install pipeline utility steps plugin, if not installed
           //here I need to configure downstram job. I have to pass package version for deployment
        // This job will wait until downstrem job is over
        stage('Deploy') {
            steps {
                script{
                    echo "Deployment"
                    
                }
            }
        }
    }

    post{
        always{
            echo 'cleaning up workspace'
            //deleteDir()
        }
    }
}