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
                sleep(5)
                echo("build 2")
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