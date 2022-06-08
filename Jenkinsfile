pipeline{
    agent any
    stages{
        stage("sonar quality check"){
            agent {
                docker{
                    image 'openjdk:11'
                }
            }
            steps{
               sh 'mvn sonar:sonar \
                -Dsonar.projectKey=CICD_Java_gradle_application \
                -Dsonar.host.url=http://65.0.20.125:9000 \
                -Dsonar.login=bca89aa09c0fda1b25e952fe82e57d25916c4682'
            }
        }
            
        
    }
}
