pipeline {
  agent any
  parameters {
        choice(
            choices: 'Backend\nFrontend\nFinal',
            description: '',
            name: 'stage_name')
    }
  stages {
    stage('Backend') {
	  when {
		expression { params.stage_name == 'Backend' }
		   
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
	}
    stage('Frontend') {
	  when {
		expression { params.stage_name == 'Frontend' }
		
      steps {
        echo 'Frontend massage'
      }
    }
	}
    stage('Final') {
      steps {
        echo 'Final'
      }
    }
  }
}