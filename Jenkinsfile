pipeline {
    agent any
    tools { 
      maven 'Maven3.9.6' 
      jdk 'Maven3.9.6' 
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
