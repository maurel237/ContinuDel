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
