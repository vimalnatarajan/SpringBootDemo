node {
   // This is to demo github action	
   def mvn = tool (name: 'maven3', type: 'maven') + '/bin/mvn'
   stage('GIT Checkout'){
    // Clone repo
	git branch: 'master', 
	credentialsId: 'github', 
	url: 'https://github.com/vimalnatarajan/SpringBootDemo'
   
   }
   stage('Mvn Package'){
	   // Build using maven
	   
	   sh "${mvn} clean package deploy"
   }
}
