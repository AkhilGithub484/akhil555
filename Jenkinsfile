pipeline {
    agent any

    stages {
        stage('stage1') {
            steps {
                echo 'Hello World this is Akhils first groovy script'
            }
        }
        stage('stage2')  {
            steps  {
                input ('Do you want to proceed:')
                }
            }
        stage('stage3') {
            when {
                not 
                {
                    branch 'master'
                     }
                 }
            steps  {
                echo 'If branch master holds false this gets executed'
                  }
             }
        stage('stage4-integration test') {
            agent {
                docker {
                    image  'ubuntu'
                     }
                 }
            steps {
                echo 'Hello World this is integration testing phase'
            }
        }
            
            
                 
                
    }
}
