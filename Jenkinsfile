pipeline {
  agent {label 'WORKSTATION'}

  stages {
    stage ('vpc') {
        sh '''
            cd vpc
            make dev-apply
        '''
    }
    stage ('db') {
        sh '''
            cd db
            make dev-apply
        '''
    }
    stage ('alb') {
        sh '''
            cd alb
            make dev-apply
        '''
    }
  }
}
