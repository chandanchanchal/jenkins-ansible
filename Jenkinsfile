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
