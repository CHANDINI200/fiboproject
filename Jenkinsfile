pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                script {
                    checkout scm
                }
            }
        }

        stage('Build and Run') {
            steps {
                script {
                    def javaHome = tool 'Java' // 'Java' is the name of the JDK configured in Jenkins

                    sh "${javaHome}/bin/javac Fibonacci.java"
                    sh "${javaHome}/bin/java Fibonacci"
                }
            }
        }
    }
}
