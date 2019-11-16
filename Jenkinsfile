ipeline {
    agent any


    stages {
        stage('SCM Checkout'){
          git 'https://github.com/pranikita/maven-project-1'
        }
  }
    {
        
		stage ('build stage') {
		             parallel {
		                    stage ('Compile Stage') {
		                    
                                steps {
                                    withMaven(maven : 'LocalMaven') {
                                        sh 'mvn clean compile'
                                    }
                                }
                            }
		                    
                            stage ('Testing Stage') {
		                    
                                steps {
                                    withMaven(maven : 'LocalMaven') {
                                        sh 'mvn test'
                                    }
                                }
                            }
						}
					}


        stage ('install Stage') {
            steps {
                withMaven(maven : 'LocalMaven') {
                    sh 'mvn install'
                }
            }
        }

         
}
}
