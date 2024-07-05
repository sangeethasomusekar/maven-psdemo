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
                sh " clean install"
      
            }
        }
        stage('deploy-dev') {
            steps {
                input 'given an approval'
                echo "deploying an appls in devo"  
            }
        }
        stage('deploy-prod') {
            steps {
                input 'given an approval'
                echo "deploying an appls in prod"     
        
            }
        }
    }
}
