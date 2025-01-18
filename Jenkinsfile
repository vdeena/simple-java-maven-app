pipeline {
    agent any
    tools { 
      maven 'Maven3.9.6' 
      jdk 'jdk11' 
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
