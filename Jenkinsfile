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
    	
    	stage ('build') {
    		steps {
    			script {
            sh "npm install"
    				sh "ansible-playbook  ansible/build.yml -i ansible/inventory/host.yml "
    			}
    		}
    	}
    
    
}
}
