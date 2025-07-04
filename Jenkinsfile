pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                dockerfile {
                    filename 'Dockerfile.build'
                    dir '.'
                }
            }
            steps {
                echo 'Etapa de compilação'
                sh 'javac Conversor.java'
            }
        }

        stage('Test') {
            agent {
                dockerfile {
                    filename 'Dockerfile.test'
                    dir '.'
                }
            }
            steps {
                echo 'Etapa de testes'
            }
        }
    }
}

