pipeline {

    agent any

    stages {
        stage("GIT Checkout") {
            steps {
                git 'https://github.com/deepanshu-rawat6/Java-CI-CD.git'
            }
        }

        stage("UNIT TESTING") {
            steps {
                sh 'mvn test'
            }
        }

        stage("INTEGRATION TESTING") {
            steps {
                sh 'mvn verify -DskipUnitTesting'
            }
        }

        stage("BUILD") {
            steps {
                sh 'mvn clean install'
            }
        }
    }
}