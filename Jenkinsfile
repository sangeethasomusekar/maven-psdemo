def sayhello(String name){
  echo "hello, ${name}."
}
pipeline {
    agent any
    
    stages {
       stage('greet') {
            steps {
                sayhello 'devops'
            }
       } 
       stage('Example Build') {
            steps {
            echo 'Hello World'
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
