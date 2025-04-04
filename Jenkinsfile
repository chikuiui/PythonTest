pipeline {   //everything is wrapped in this.   
    agent {  // we select the agent that we want this job to run on.
        node {
            label 'docker-agent-alpine'   // specifying based on label.
            }
      }
    // triggers {
    //     pollSCM '*/5 * * * *'  // means every 5 minutes
    // }
    stages {    // contain individual stages having 3 stage pipeline
        stage('Build') {
            steps {
                echo "Building.."
                sh '''
                echo "doing build stuff.."
                '''
            }
        }
        // If test stage fail then the below other stages also fail.
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                echo "doing test stuff.."
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver....'
                sh '''
                echo "doing delivery stuff.."
                '''
            }
        }
    }
}
