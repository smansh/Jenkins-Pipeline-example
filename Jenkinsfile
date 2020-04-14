node {
   stage('SCM Checkout'){
	git: 'https://github.com/smansh/Jenkins-Pipeline-example'   
   }
   stage('Compile Package'){
   //Get MavenHome path
      def mvnHome = tool name: 'Maven_home', type: 'maven'
       sh "${mvnHome}/bin/mvn package"
       }
   }
