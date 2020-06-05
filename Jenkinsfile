node {
   stage('SCM Checkout'){
	git 'https://github.com/smansh/Jenkins-Pipeline-example'   
   }
   stage('Compile Package'){
   //Get MavenHome path
      def mvnHome = tool name: 'Maven_home', type: 'maven'
       sh "${mvnHome}/bin/mvn package"
       }
	//Add Email Notification
	stage('Email-Notification'){
	
		mail bcc: '', body: '''Hi,
Welcome to Jenkins job Email Alert
Thanks,
Manoj''', cc: '', from: '', replyTo: '', subject: 'Jenkinsfile-Build-Pipeline', to: 'manoj.himt@gmail.com'
	}
	//Slack  Notification
	stage('Slack-Notification'){
	slackSend baseUrl: 'https://hooks.slack.com/services/',
	channel: 'jenkins-pipeline-demo', 
	color: 'good', 
	message: 'Welcome to Jenkins Slack Build SucessFully !!!',
	teamDomain:'smansh-jenkinsteam',
	tokenCredentialId: 'slack-notify'
	}
   }
