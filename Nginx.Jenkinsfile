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
    docker rm -f nginx5 | exit 0
    docker run -d -p 8999:80 --name nginx5 nginx5
    echo "hi"
    '''
     }
    } 
  }
}
    
