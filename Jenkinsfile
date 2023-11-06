pipeline {
    agent any 
    stages {
        stage('clonings') { 
            steps {
               echo "cloning"
                git branch: 'main', credentialsId: 'access_token_github', url: 'https://github.com/said1024/jenkins3.git'
            }
        }
 stage('maven build') { 
            steps {
               echo "build"
                sh "mvn clean package"
            }
        }

stage('deploy') {
            steps {
                echo "deploy"
               // sh "java -jar $WORKSPACE'/target/optidial-0.0.1-SNAPSHOT.jar'"
            }
        }
 

    }
}
