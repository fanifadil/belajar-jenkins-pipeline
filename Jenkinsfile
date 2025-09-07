pipeline {
    agent {
        node {
            label "linux && java17"
        }
    }
    stages {
        stage("Build") {
            steps {
                echo("Start build")
                sh("./mvnw clean compile test-compile")
                echo("Finish finish")
            }
        }
        stage("Test") {
            steps {
                echo("test build")
                sh("./mvnw test")
                echo("test finish")
            }
        }
        stage("Deploy") {
            steps {
                echo("deploy 1")
            }
        }
    }
}