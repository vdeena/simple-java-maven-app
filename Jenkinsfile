pipeline {
    agent any
    tools { 
      maven 'Maven3.9.6' 
      jdk 'jdk-21.0.5' 
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }  
    }
          
}
