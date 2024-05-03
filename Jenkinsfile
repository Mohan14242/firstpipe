@Library('roboshop') _

pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                script {
                    def param1 = "value1"
                    def param2 = "value2"
                    def result = mySharedFunction(param1, param2)
                    println "Result: ${result}"
                }
            }
        }
    }
}
