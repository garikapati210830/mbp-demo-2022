
pipeline {
  agent any
  tools {
  maven 'maven3'
   }
  
  stages {
    stage('Maven Build') {
      when{
        branch 'develop'
      }
      steps {
        sh 'mvn clean package'
      }
    }

      stage('Sonar Analysis') {
      when{
        branch 'develop'
      }
      steps {
        echo "sonar analysis"
      }
    }
     
stage('Upload to  Nexus') {
      when{
        branch 'develop'
      }
      steps {
        echo "upload to nexus"
      }
    }

       stage('Deploy to Dev and test') {
      when{
        branch 'develop'
      }
      steps {
       echo "Deploy to development...."
       echo "Deploy to test...."
      }
    }

 stage('Deploy to UAT') {
      when{
        branch 'uat'
      }
      steps {
       echo "Deploy to uat...."
       
      }
    }

stage('Deploy to Production') {
      when{
        branch 'master'
      }
      steps {
       echo "Deploy to Production...."
       
      }
    }

   
  }
  
}
