def sayhello(string name){
    echo "hello, ${name}."

pipeline {
    agent any
    
    stages {
        stage('Example Build') {
            steps {
            echo 'Hello World'
            }
        
       }
       stage('greet') {
            steps {
                sayhello 'devops'
            }
        } 
        stage('Example Deploy') {
            when {
                branch 'production'
            }
            steps {
                echo 'Deploying'
            }
        }
    }
}
