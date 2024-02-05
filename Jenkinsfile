pipeline {
    agent {
        node {
            label 'AGENT1'
        }
    }

    options {
        timeout(time: 1, unit: 'SECONDS')
    }

    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
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
        // sh 'sleep 10s'
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
    aborted {
        echo "aborted due to timeout exception"
    }
   }
}