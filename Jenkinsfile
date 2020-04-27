pipeline {
    
    agent any
    
    tools{
        maven 'mvn3'
    }
    
    stages{
        
        stage ('git pull/checkout'){
            
            steps {
                git 'https://github.com/java2786/bamboo-git-maven-tomcat'
            }
            
        }
        
        stage ('compile') {
            steps {
                bat label: '', script: 'mvn clean compile'
            }
        }
        
        stage ('build'){
            steps {
                bat label: '', script: 'mvn package'
            }
        }
        
    }
    
}
