pipeline {
    agent any 
    stages {
        stage('Build satge') { 
            steps { 
                wihtMaven(maven : 'maven_3_5_0') {
                    sh 'mvn clean compile'
                }
                 
            }
        }
        stage('Testing stage') { 
            steps { 
                withMaven(mave : 'maven_3_5_0') {
                    
                    sh 'mvn test'
                }
                 
            }
        }
        stage('Deploymnet stage') { 
            steps { 
                withMaven(maven : 'maven_3_5_0') {
                    sh 'maven deploy'
                }
                 
            }
        }
    }
}
