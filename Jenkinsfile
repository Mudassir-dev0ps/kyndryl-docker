pipeline {
       
        stages {
                stage('create image') {
                        steps {
                                sh 'docker build -t pipeimage .'
                        }
                
                     }

		           stage('tag image') {
                        steps {
                                sh 'docker tag msmengr/pipeimage pipeimage'
                        }
                
                     }

		          stage('push image') {
                        steps {
                                sh 'docker login -u msmengr -p !2bcought'
                        }
                
                     }

               stage('create container') {
                        steps {
                                sh 'docker run -dit --name mudassir pipeimage'
                        }
                
                     }
                }
       }
