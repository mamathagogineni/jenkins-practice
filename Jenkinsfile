pipeline {
    agent {
        node {
            label 'AGENT1'
        }
    }

    options {
        timeout(time: 1, unit: 'SECONDS')
    }
    
    stages {
     stage ('build') {
        steps {
        echo "building..."
        }
    }
    stage ('test') {
        steps {
        echo "testing..."
        }
    }
    stage ('deploy') {
        steps {
        echo "deploying..."
        sh 'sleep 10s'
        }
    }
    }

   post {
    success {
        echo "build is success"
    }
    always {
        echo "Always say hiiiii"
    }
    failure {
        echo "Build got failed"
    }
   }
}