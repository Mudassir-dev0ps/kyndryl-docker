pipeline {
       
        stages {
                stage('create image') {
                        steps {
                                sh 'docker build -t pipeimage .'
                        }
                
                     }

		           stage('tag image') {
                        steps {
                                sh 'docker tag msmengr/pipeimage pipeimage:v1'
                        }
                
                     }

		          stage('push image') {
                        steps {
                                sh 'docker login -u msmengr -p koenig123'
                        }
                
                     }

               stage('create container') {
                        steps {
                                sh 'docker run -dit --name mudassir pipeimage'
                        }
                
                     }
                }
       }
