pipeline {
    agent{
        label 'master'
    }
    environment {
        appName = "variable"
    }
    stages{
        stage("PASO 1") {
            steps {
                echo "HOLA DESDE JK"
                script {
                    sh "echo 'HOLA DESDE SH JK'"
                }
            }
        }
    }
    post {
        always {
            deleteDir()
            sh "echo 'FASE always'"
        }
        success {
            sh "echo 'FASE success'"
        }
        failure {
            sh "echo 'FASE failure'"
        }
    }

}