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
            sh "sudo curl -sL https://deb.nodesource.com/setup_16.x | bash -"
            sh "sudo apt-get install nodejs -y"
            sh "node --version"
            sh "sudo npm install npm@latest -g"
            sh "sudo npm --version"
            sh "sudo npm install -g @angular/cli"
            sh "ng version"
    				sh "ansible-playbook  ansible/build.yml -i ansible/inventory/host.yml "
    			}
    		}
    	}
    
    
}
}
