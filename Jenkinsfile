pipeline{
  agent any
  triggers {
    cron('H/05 * * * *')
  }
  stages {
    stage("Build"){
      steps{
        bat 'gradle build'
      }
    }
    stage("Test"){
      steps{
        bat 'gradle clean apiFeatures -Ptags="@Calculadora"'
      }
    }
  }
}
