pipeline {
    agent any

    tools {
        
        maven "mvn"
    }
    stages {
        stage('prepare') {
            steps {
               git 'https://github.com/jglick/simple-maven-project-with-tests.git'
            }
        }
        stage('build') {
            steps {
                sh "mvn clean install"
      
            }
        }
        stage('bdeploy-dev') {
            steps {
                input 'given an approval'
                echo "deploying an appls in devo"  
            }
        }
        stage('bdeploy-sprod') {
            steps {
                input 'given an approval'
                echo "deploying an appls in prod"       
            }
        }
    }
}
