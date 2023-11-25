pipeline{
agent(label 'Jenkins-Agent')
tools  {
    jdk 'Java17'
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
           ssh 'mvn clean package'
       }
    }
     stage('testapplication'){
       steps{
           ssh 'mvn test'
       }
    }
}
}
