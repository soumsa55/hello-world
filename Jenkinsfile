pipeline{
  agent {label 'DevOpsAgent'}
  tools{
    jdk 'Java21'
    maven 'Maven3'
  }
  stages{
    stage('Clean Workspace'){
      steps{
        cleanWs()
      }
    }
    stage('Checkout from SCM'){
      steps{
        git branch: 'master' , credentialsId: 'github' , url: 'https://github.com/soumsa55/hello-world'
      }
    }
    stage('Build application'){
      steps{
        sh 'mvn clean package'
      }
    }
     stage ('Test Application'){
       steps{
         sh 'mvn test'
       }
     }
  }
}
