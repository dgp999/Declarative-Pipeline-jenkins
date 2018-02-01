pipeline {
  agent any
  parameters {
        choice(
            choices: 'Backend\nFrontend',
            description: '',
            name: 'Stage_Name')
    }
  stages {
    stage('Backend') {
        when {
                
                expression { params.Stage_Name == 'Backend' }
            }
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
        when {
                
                expression { params.Stage_Name == 'Frontend' }
            }
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
