pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building..'
        // Here you can define commands for your build
    }
}
stage('Test') {
  steps {
    echo 'Testing..'
    // Here you can define commands for your tests
  }
}
stage('Deploy') {
  steps {
    echo 'Deploying....'
    // Here you can define commands for your deployment
  }
}
}
  post {
    //the conditions will go here after the build is done
      post {
        //inevitable action
        echo 'Post build condition running'
      }
      failure {
        //this action will happen only if the build has failed
        echo 'Post action if build has failed...'
      }
  }
  
}
