pipeline{
    agent{label 'master'}
    tools{maven 'M3'}
    stages {
        stage('Checkout') {
            steps {
                git branch:'main',
                url:'https://github.com/VINOD043/SpringPetClinic.git' 
            }
        }
        stage('Build') {
            steps {
                bat 'mvn compile'
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
        stage('Package') {
            steps {
                bat 'mvn package'
            }
        }
        stage('Deploy') {
            steps {
                bat 'java -jar C:\\ProgramData\\Jenkins\\.jenkins\\workspace\\PetClinicDeclarativePipeline\\target\\spring-petclinic-2.1.0.BUILD-SNAPSHOT.jar'
            }
        }
    }
}
