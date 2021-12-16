pipeline {

    agent any


      stages {
          stage ('pull') {
                steps {
                   script{
                       checkout([$class: 'GitSCM', branches: [[name: '*/master']],
                           userRemoteConfigs: [[
                               credentialsId: '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',
                               url: 'https://github.com/maurel237/ContinuDel.git']]])

                
            }
        }
    }
    	
    	
    
    
}
}
