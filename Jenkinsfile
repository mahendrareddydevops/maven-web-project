pipeline {
    agent 'jenkins_agent'
	tools {
		jdk "Java_home" 
maven "Maven_Home"
}
    stages {
        stage('checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'Github', url: 'https://github.com/mahendrareddydevops/maven-web-project.git']]])
            }
        }
        stage('validate') {
            steps {
                bat 'mvn validate'
            }
			}
            stage('compile') {
                steps {
                    bat 'mvn compile'
                }
				}
                stage('install') {
                    steps {
                        bat 'mvn install'
                    }
					}
                    stage('test') {
                        steps {
                            bat 'mvn test'
                        }
						}
                        stage('package') {
                            steps {
                                bat 'mvn package'
                            }
                            }
                        
                        
                                       
               }
                }
            
    

