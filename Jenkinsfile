pipeline{
  agent any
  stages{
        stage('Clone repository'){
          steps {
            checkout([$class:'GitSCM',
            branches: [[name: '*/main']],
            userRemoteConfigs: [[url: 
