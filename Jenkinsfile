Pipeline{
    agent any
    stages{
        stage("sonar_quality_check"){
            agent{
                docker{
                    image 'openjdk:11'
                }
            }
            steps{
                script{
                    withSonarQubeEnv(credentialsId: 'sonar-final') {
                            sh 'chmod +x gredlew'
                            sh './gradlew sonarqube'
                    }
                }
            }
        }
    }
}
