pipeline {
  agent any
  stages {
        stage('Checkout') {
            steps {
               

                checkout([$class: 'GitSCM',
                          branches: [[name: '*/main']],
                                extensions: [[$class: 'CleanCheckout']],
                                userRemoteConfigs: [[url: 'https://github.com/chandanchanchal/jenkins-ansible']]
                       ])

            }
        }
        
        stage('Ansible Init'){
         steps{
          script{
           def aHome = tool name: 'Ansible'
           env.PATH = "${aHome}:${env.PATH}"
           sh 'ansible --version'
          }}
        }
    }
    
}
