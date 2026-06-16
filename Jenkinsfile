pipeline{
  agent any
  tools{
    maven 'Maven'
  }
  stages{
    stage('Checkout'){
      steps{
        git branch:'master',
          url:'https://github.com/Ranjana2225/ranju-webapp.git'
      }
    }
    stage('Build'){
      steps{
        sh 'mvn clean install'
      }
    }
    stage('Debug') {
    steps {
        sh 'whoami'
    }
}
    stage('Deploy with ansible'){
      steps{
        sh 'ansible-playbook deploy.yml'
      }
    }
  }
}
    
