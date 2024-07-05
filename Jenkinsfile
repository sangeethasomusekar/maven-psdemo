pipeline {
    agent {label, 'maven-label'}

    stages {
        stage('prepare') {
            steps {
                git branch: 'main', url: 'https://github.com/sangeethasomusekar/maven-psdemo.git'
            }
        }
        stage('build') {
            steps {
                sh 'mvn clean install'
            }
        }   
        stage('deploying-dev') {
            steps {
                echo 'deploying an appln in devo'
            }
        }   
        stage('deploying-stage') {
            steps {
                input 'give an approval'
                echo 'deploying an appln in stage'
            }
        }   
        stage('deploying-prod') {
            steps {
                input 'give an approval'
                echo 'deploying an appln in prod'
            }
        }   
    }
}
