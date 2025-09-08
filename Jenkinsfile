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
            steps {
                echo("deploy 1")
            }
        }
    }
}