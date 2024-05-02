pipeline {
    agent any

    stages {
        stage('Version') {
            steps{
                script{
                def env.Version=readJSON(file: 'package.json').version
                }
            }
    }
    }
}
