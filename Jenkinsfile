pipeline
{
	agent any
	  stages{
	      stage('Pull'){
	           steps{
	              script(
	                  checkout([$class: 'GitSCM' , branches : [[name : '*/master']],
	                  userRemoteConfigs : [[
	                  	credentialsId : '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',
	                  	url : 'https://github.com/maurel237/ContinuDel.git']]
	                  	 ]
	                  	)
	              )
	           }
	      }
	  }


}
