pipeline {
    agent {
        node {
            label "linux && java17"
        }
    }
    stages {
        stage("Build") {
            steps {
                echo("build 1")
            }
        }
        stage("Test") {
            steps {
                echo("test 1")
            }
        }
        stage("Deploy") {
            steps {
                echo("deploy 1")
            }
        }
    }
}