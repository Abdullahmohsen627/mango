pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'build completed...'
      }
    }

    stage('test stage') {
      parallel {
        stage('test 2') {
          steps {
            echo 'test completed'
          }
        }

        stage('test 1') {
          steps {
            echo 'running test1'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        input(message: 'Are you sure?', ok: 'ok,iam sure')
        echo 'deployment completed..'
      }
    }

  }
}