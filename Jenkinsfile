pipeline {
    agent any
    
    environment{
        EXAMPLEEV = 'Echo and The Bunnymen'
    }
    
//    options {
//        skipStagesAfterUnstable()
//    }
    
    stages {
       stage('Echo and the Bunnymen') {
            agent any
            steps { 
                {
                    echo "${EXAMPLEEV}"
                }
            }
        }
    }
    post {
        always{
            echo 'Running JUnit tests'
//            junit 'build reports/**/*.xml' 
        }
        success{
            echo 'Success on a plate for you'
        }
        failure{
            echo 'Houston, we have a problem'
        }
        changed{
            echo 'The status has changed since the last build'
        }
    }
}
