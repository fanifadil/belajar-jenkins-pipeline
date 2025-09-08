pipeline {
    agent none
    stages {
        stage("Build") {
            agent {
                node {
                    label "linux && java17"
                }
            }
            steps {
                echo("Start build")
                sh("./mvnw clean compile test-compile")
                echo("Finish finish")
            }
        }
        stage("Test") {
            agent {
                node {
                    label "linux && java17"
                }
            }
            steps {
                script {
                    def data = [
                        "firstName" : "Fani",
                        "lastName" : "Fadil"
                    ]
                    writeJSON(file: "data.json", json:data)
                }
                echo("test build")
                sh("./mvnw test")
                echo("test finish")
            }
        }
        stage("Deploy") {
            agent {
                node {
                    label "linux && java17"
                }
            }
            steps {
                echo("deploy 1")
            }
        }
    }
}