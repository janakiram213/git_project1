node {
   stage ('SCM Checkout'){
     git 'https://github.com/janakiram213/git_branch_project'
   }
   stage ('validate'){
     //get maven home path
     def mvnHome = tool name: 'maven-3', type: 'maven'
     sh "${mvnHome}/bin/mvn validate"
    }

   stage ('Compile'){
     //get maven home path
     def mvnHome = tool name: 'maven-3', type: 'maven'
     sh "${mvnHome}/bin/mvn compile"
    }
   stage ('test'){
     //get maven home path
     def mvnHome = tool name: 'maven-3', type: 'maven'
     sh "${mvnHome}/bin/mvn test"
    }
   stage ('package'){
     //get maven home path
     def mvnHome = tool name: 'maven-3', type: 'maven'
     sh "${mvnHome}/bin/mvn package"
    }
  /*stage ('deploy to tomcat'){
      sshagent(['d1a165b8240f63c9b0261e49ace77cb0d119e6ad']) {
          sh 'scp -o StrictHostKeyChecking=no target/*.war jenkins@172.31.95.95:/opt/tomcat/webapps'
    }
  }*/
}    

