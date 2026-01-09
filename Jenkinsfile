pipeline {
    
    agent any
    tools {maven "mavenV4"}
    stages{
        
        stage("checkout"){
            
            steps{
                git branch:"main", url: "https://github.com/sthakkasilaaltimetrik/SpringRESTful.git"
            }
        }
        
        stage("build"){
            
            steps{
                sh "mvn compile"
            }
        }
        
        stage("test"){
            
            steps{
                
                sh "mvn test"
            }
        }
        
        stage("package"){
            
            steps{
                
                sh "mvn package"
            }
        }
        
        stage("deploy"){
            
            steps{
                
                sh "java -jar ./target/*.jar"
            }
        }
    }
}
