pipeline {
    agent { label, 'maven-label' }

    }
    stages {
        stage('prepare') {
            steps {
               git branch: 'main', url:'https://github.com/jglick/simple-maven-project-with-tests.git'
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
                echo "deploying an appln in devo"  
            }
        }
        stage('deploy-stage') {
            steps {
                input 'given an approval'
                echo "deploying an appls in stage"  
            }   
        } 
        stage('deploy-prod') {
            steps {
                input 'given an approval'
                echo "deploying an appln in prod"            
            }
        }
    }
}
