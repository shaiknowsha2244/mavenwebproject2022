pipeline {
    agent any 
	tools {
          jdk 'JAVA_HOME'
              }
     stages {
        stage('Checkout') { 
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-github', url: 'https://github.com/shaiknowsha2244/mavenwebproject2022.git']]]) 
            }
        }
        stage('Build') { 
            steps {
                sh 'mvn compile' 
            }
        }
        stage('Test') { 
            steps {
               sh 'mvn test' 
            }
        }
		 stage('package') { 
            steps {
               sh 'mvn package' 
            }
        }
    }
}
