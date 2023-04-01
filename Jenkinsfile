pipeline {
    agent any
    stages {
        stage("Hello Server") {
            steps {
                echo("Hello Pipeline")
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