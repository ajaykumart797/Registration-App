pipeline{
agent{label 'Jenkins-Agent'}
tools  {
    jdk 'jdk17'
    maven 'maven3'
  }
  stages{
    stage(' clean workspace ')
    {
      steps{
        cleanWs()
      }
    }
    stage('git checkout'){
       steps{
           git branch: 'main', url: 'https://github.com/ajaykumart797/Registration-App.git'
       }
    }
     stage('build application'){
       steps{
           sh 'mvn clean package'
       }
    }
     stage('testapplication'){
       steps{
           sh 'mvn test'
       }
    }
}
}
