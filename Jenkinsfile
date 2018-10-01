pipeline {
  agent {
    node {
      label 'Agent_UrbanCode_T3'
    }

  }
  stages {
    stage('Download Source') {
      parallel {
        stage('Download Source') {
          environment {
            Dev = 'Dev'
          }
          steps {
            svn(poll: true, url: 'file:///E:/SvnRepo')
          }
        }
        stage('Build') {
          steps {
            build 'HelloWoldDemo'
          }
        }
      }
    }
  }
}