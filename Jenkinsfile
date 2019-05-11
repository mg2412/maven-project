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

    }
}
