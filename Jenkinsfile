pipeline{
    agent{
        docker {
            image 'maven:3.8.1-adoptopenjdk-11'
            args '-v /root/.m2:root/.m2'
        }
    }
    stages{
        stages('Build'){
            steps{
                sh 'mvn -B -DskipTests clean package'
            }
         }
        stages('Test'){
            steps{
                sh 'mvn test'
            }
        }
        stages('QA'){
            steps{
                echo 'QA'
            }
        }
    }
}