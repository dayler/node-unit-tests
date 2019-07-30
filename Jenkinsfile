pipeline {
    agent none
    
    options {
        buildDiscarder logRotator (daysToKeepStr: '8', numToKeepStr: '5')
    }
    
    environment {
        MyKeyId="myCustomValue1"
    }
    
    stages {
        
        stage('Descargar codigo fuente') {
            environment {
                MyKeyId="myCustomValue1x"
            }
            // when {
            //     branch "master"
            // }
            steps {
                script {
                    node {
                        println "\n Mi primer statge.\n MyKeyId value es: ${MyKeyId}\n"
                    }
                }
            }
        }
        
        stage('test') {
            steps {
                script {
                    node {
                        sh "echo '\nMi segundo stage esta en ejecucion. KeyId:$MyKeyId\n'"
                    }
                }
            }
        }
    }
}
