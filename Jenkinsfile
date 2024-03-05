pipeline{
  agent any
  stages{
    stage("Build"){
      steps{
        build 'PES1UG21CS699-1'
        sh 'g++ new.cpp -o new'
      }
    }
    stage("Test"){
      steps{
        sh './new'
      }
    }
    stage("Deploy"){
      steps{
        echo 'Deploy'
      }
    }
  }
  post{
    failure{
      error 'Pipeline failed'
    }
  }
}
