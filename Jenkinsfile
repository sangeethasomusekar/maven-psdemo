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
        <plugin>
			<groupId>org.apache.maven.plugins</groupId>
			<artifactId>maven-surefire-plugin</artifactId>
		    <version>2.19.1</version>
			<configuration>
    		<testFailureIgnore>true</testFailureIgnore>
			</configuration>
		</plugin>          
            }
        }
    }
}
