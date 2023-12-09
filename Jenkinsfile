pipeline{
  agent any

  environment{
    REACT_DIR = 'nie'
  }

  tools{
    nodejs "Node_20.10.0"
  }

  stages{
    stage('Check out'){
      steps{
        checkout scm
      }
    }

    stage('npm install'){
      steps{
        dir("${env.REACT_DIR}"){
          sh 'npm install'
        }
      }
    }

    stage('build'){
      steps{
        dir("${env.REACT_DIR}"){
          sh 'npm run build'
        }
      }
    }

    // stage('test'){
    //   steps{
    //     sh 'npm run test'
    //   }
    // }
  }
}
