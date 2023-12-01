flag-true
pipeline {
  agent any
  parameters { 
  //these are types of parameters 
    string(name: 'VERSION', defaultvalue:'' , description: 'version to deploy on prod')
    choice (name: 'VERSION', choices: ['1.1.0', '1.2.0', '1.3.0'], description:'')
    booleanParam(name:'executeTests', defaaltvalue: true, description:'')
  environment {
    NEW_VERSION = '1.3.0'
  }
  stages {
    stage('Build') {
      steps {
        echo "Building Project ${NEW_VERSION}"
        // Here you can define commands for your build
    }
}
stage('Test') {
  when {
    expression {
        params.executeTests
      }
  }
    echo 'Testing project...'
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
      always {
        //inevitable action
        echo 'Post build condition running'
      }
      failure {
        //this action will happen only if the build has failed
        echo 'Post action if build has failed...'
      }
  }
  
}
