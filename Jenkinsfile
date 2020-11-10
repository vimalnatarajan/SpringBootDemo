node {
   // This is to demo github action	
   
   stage('GIT Checkout'){
    // Clone repo
	git branch: 'master', 
	credentialsId: 'github', 
	url: 'https://github.com/vimalnatarajan/SpringBootDemo'
   
   }
   stage('Mvn Package'){
	   // Build using maven
	   def mvn = tool (name: 'maven3', type: 'maven') + '/bin/mvn'	   
	   sh "${mvn} clean package deploy"
   }
}
