pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('dev') {
      parallel {
        stage('dev') {
          steps {
            echo 'develop'
          }
        }
        stage('abc') {
          steps {
            sh 'echo \'hello\''
          }
        }
      }
    }
  }
  environment {
    a = 'b'
  }
  parameters {
    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
    text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
    booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
    choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
    password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
  }
}