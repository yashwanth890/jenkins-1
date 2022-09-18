pipeline {
  agent any
  stages {
    stage('Tool version log') {
      steps {
        sh '''mvn --version
git --version
jenkins --version
java -version'''
      }
    }

    stage('Build with Maven ') {
      steps {
        sh 'mvn compile test package'
      }
    }

    stage('Post Build test') {
      steps {
        writeFile(file: 'Result.txt', text: 'Successfully Done')
      }
    }

  }
}