pipeline {
    agent any

    stages {
        stage('Version') {
            env.Version=readJSON(file: 'package.json').version
    }
    }
}
