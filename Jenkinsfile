pipeline {
    agent {
        label 'AGENT-1'
    }
    options {
        timeout(time: 30, unit: 'MINUTES')
        disableConcurrentBuilds()
        ansiColor('xterm')
    }
    parameters{
        string(name: 'appVersion', defaultValue: '1.0.0', description: 'what is the application?')
    }
    environment{
        def appVersion = '' //variable declaration
        //nexusUrl = 'nexus.bnsaws.online:8081'
          nexusUrl = '204.236.215.167:8081'

    stages {
        stage('print the version'){
            steps{
                script{
                     echo "Application Version: = ${params.appVersion}" 
                   

              }
           }
        }
                    


    
        post { 
        always { 
            echo 'I will always say Hello again!'
            deleteDir()
        }
        success { 
            echo 'I will run when pipeline is success'
        }
        failure { 
            echo 'I will run when pipeline is failure'
        }
    }
}
    }