pipeline {
    agent any
    stages{
        stage(scm){
            steps{
                git 'https://github.com/bingoassistance/Spring-petclinic-project1.git'
            }
        }
        
        stage(build){
            steps{
                sh '''
                mvn clean install
                '''
            }
        }

        stage(imagebuild){
            steps{
                sh '''
                sudo docker build -t test .
                '''
            }
        }
    }
}
 
