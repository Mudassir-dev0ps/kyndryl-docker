pipeline {
	agent any
       
        stages {
                stage('create image') {
                        steps {
                                sh 'docker build -t pipeimage .'
                        }
                
                     }

		           stage('tag image') {
                        steps {
                                sh 'docker tag pipeimage msmengr/pipeimage '
                        }
                
                     }

		          stage('push image') {
                        steps {
                                sh 'docker login -u msmengr -p Koenig123'
								sh 'docker push msmengr/pipeimage'
                        }
                
                     }

               stage('create container') {
                        steps {
                                sh 'docker run -dit --name mudassirqic msmengr/pipeimage'
                        }
                
                     }
                }
       }
