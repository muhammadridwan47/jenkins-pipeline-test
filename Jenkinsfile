pipeline {
    agent any
    stages {
        stage("Build") {
            steps {
                echo("on Build")
            }
        }
        stage("Test") {
            steps {
                echo("on Test")
            }
        }
        stage("Deploy") {
            steps {
                echo("on Deploy")
            }
       }
    }

    // post run after the task excuted
    post {
        always {
            echo "always run in any condition"
        }
        success {
            echo "running when the pipline status success"
        }
        failure {
            echo "running when the pipline status error"
        }
        cleanup {
            echo "don't care success or error"
        }
    }
}
