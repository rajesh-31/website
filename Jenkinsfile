pipeline {
    agent any
    tools {
        maven 'maven3'
    }


    stages {
        stage('Checkout') {
            steps {
                checkout poll: false, scm: scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/rajesh-31/website.git']])
            }
        }

        stage('Build') {
            steps
               sh 'mvn package'
            }
        }
    }
}
