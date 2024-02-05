pipeline {
    agent {
        node {
            label 'AGENT1'
        }
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
   }
}