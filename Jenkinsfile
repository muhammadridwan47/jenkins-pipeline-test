@Library('shared-library-jenkins') _

import classschema.jenkins.Output;

pipeline {
    agent any
    stages {
        stage("Build") {
            steps {
                script {
                    welcome.world()
                }             
                echo("on Build")
            }
        }
        stage("Test") {
            steps {
                 script {
                    Output.hello(this, "Komang James")
                }  
                echo("on Test")
            }
        }
        stage("Deploy") {
            steps {
                echo("on Deploy")
            }
       }
    }

    // post runs after the task excuted
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
