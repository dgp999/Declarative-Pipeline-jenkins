pipeline {
  agent any
  stages {
    stage('Backend') {
      steps {
        parallel(
          "Backend": {
            echo 'backend message '
            
          },
          "Backend2": {
            echo 'backend2'
            
          },
          "Backeend": {
            echo 'backend3'
            
          }
        )
      }
    }
    stage('Frontend') {
      steps {
        echo 'Frontend massage'
      }
    }
    stage('Final') {
      steps {
        echo 'Final'
      }
    }
  }
}