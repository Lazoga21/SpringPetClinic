pipeline{
    agent{label 'any'}
    tools{maven 'M3'}
    stage{
        stage('Checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/Lazoga21/SpringPetClinic.git'
            }
        }
        stage('Build'){
            steps{
                sh 'mvn compile'
            }
        }
        stage('test'){
            steps{
                sh 'mvn test'
            }
        }
        stage('Package'){
            steps{
                sh 'mvn package'
            }
        }
        stage('Deploy'){
            steps{
                sh 'java -jar /home/coder/.jenkins/workspace/PetClinicDeclarativePipeline/target/*.jar'
            }
        }
    }
}
