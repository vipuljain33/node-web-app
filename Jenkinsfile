pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Running build automation'

            }
        }
        stage('Build Docker Image')
        {
            when
            {
                branch 'master'
            }
            steps{
                script{
                    app = docker.build("vipuljain33/node_web_app")
                    app.inside
                    {
                        sh 'echo $(curl localhost:8080)'
                    }
                }
            }



        }
    }
}