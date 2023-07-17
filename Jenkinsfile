pipeline {
    agent {
        label 'master'
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                script {
                    withCredentials([string(credentialsId: 'dockerhub', variable: 'DOCKERHUB')]) {
                        sh """
                            echo 'Building..'
                            export DOCKERHUB=\$DOCKERHUB
                            echo \$DOCKERHUB
                        """
                    }
                }
            }
        }
    }
}
