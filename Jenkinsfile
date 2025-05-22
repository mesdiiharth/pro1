pipeline {
    agent any
    stages{
        stage('build project'){
            steps{
                git url:'https://github.com/mesdiiharth/pro1/', branch: "master"
                sh 'mvn clean package'
              
            }
        }
        stage('Build docker image'){
            steps{
                script{
                    sh 'docker build -t mesiddharth07/staragileprojectfinance:v1 .'
                    sh 'docker images'
                }
            }
        }
         
        
     stage('Deploy') {
            steps {
                sh 'sudo docker run -itd --name My-first-containe2121 -p 8083:8081 mesiddharth07/staragileprojectfinance:v1'
                  
                }
            }
        
    }
}
