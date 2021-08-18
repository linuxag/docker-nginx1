pipeline{
    agent{label "worker1"} 
    stages{
    stage("build"){
    steps{
    sh '''
    docker build -t nginx5 -f Dockerfile .
    '''
     }
    } 
    stage("run"){
    steps{
    sh '''
    docker run -d -p 8999:80 nginx5
    '''
     }
    } 
  }
}
    
