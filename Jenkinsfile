pipeline {
    agent none
    environment {
        AUTHOR = "FANI FADIL"
        EMAIL = "fanifadil75@gmail.com"
    }
    stages {
        stage("Prepare") {
            agent {
                node {
                    label "linux && java17"
                }
            }
            steps {
                echo("author: ${AUTHOR}")
                echo("email: ${EMAIL}")
                echo("JOB_NAME : ${env.JOB_NAME}")
                echo("BUILD_NUMBER : ${env.BUILD_NUMBER}")
                echo("BRANCH_NAME : ${env.BRANCH_NAME}")
            }
        }
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