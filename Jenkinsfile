pipeline{
  agent any
  stages{
        stage('Clone repository'){
          steps {
            checkout([$class:'GitSCM',
            branches: [[name: '*/main']],
            userRemoteConfigs: [[url: 'https://github.com/smriti170503/PES2UG21CS519_Shweta-.git']]])
          }
        }
     stage('Build'){
       steps{
         build 'PES2UG21CS519-1'
         sh 'g++ hello.cpp -o output'
       }
     }
     stage('Test'){
       steps{
         sh './output'
       }
     }
     stage('Deploy'){
       steps{
         echo 'deploy'
       }
     }
  }
  post{
    failure{
      error 'Pipeline failed'
    }
  }
}
