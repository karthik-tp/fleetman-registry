node {
   stage('Preparation') { 
      git 'https://github.com/karthik-tp/fleetman-registry'
   }
   stage('Build') {
  
         sh "mvn package"
      
   }
   stage('Results') {
      junit '**/target/surefire-reports/TEST-*.xml'
      archive 'target/*.jar'
   }
}
