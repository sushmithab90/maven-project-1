  
pipeline {
    agent any


    stages {
        stage('SCM Checkout'){
          git 'https://github.com/prakashk0301/maven-project.git'
        }
  }
    {
        stage ('Test Stage') {
            steps {
                withMaven(maven : 'LocalMaven') {
                    sh 'mvn clean test'
                }
            }
        }
    }
}	
		
		
