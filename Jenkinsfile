pipeline {
    agent any

    stages {
        stage('SCM-Stage'){
                steps {
                    echo 'Pulling Source Code from Version Control'
                    sh "rm -rf gittest"
                    sh "git clone https://github.com/BharatYadav2000/gittest.git"
                    echo 'Pulling Source Code completed successfully !!'
                }
            }
        stage('Process') {
            steps {
                sh "pwd"
                sshagent(['ssh-key']){
                    sh "scp -o stricthostkeychecking=no gittest/file1.txt ubuntu@54.75.36.163:/home/ubuntu/aws"
                }
            }
        }
    }
}
