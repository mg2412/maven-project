pipeline {
    agent any

    stages {
        stage ('Checkout') {

            steps {
                git 'https://github.com/mg2412/maven-project.git'
                }
            }
        

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'localMaven') {
                    sh 'mvn test'
                }
            }
        }

stage ('package Stage') {

            steps {
                withMaven(maven : 'localMaven') {
                    sh 'mvn package'
                }
            }
        }
        
stage ('install Stage') {

            steps {
                withMaven(maven : 'localMaven') {
                    sh 'mvn install'
                }
            }
        }
 //       stage ('deploy Stage') {

   //         steps {
     //           sshagent (credentials: ['8d3a7cbf-062b-4fb2-811e-5f8be9635fb5']) {
       //         sh 'scp -o StrictHostKeyChecking=no */target/*.war ec2-user@172.31.22.217:/var/lib/tomcat/webapps'
         //     }
           // }
    //    }
        
    }
}
