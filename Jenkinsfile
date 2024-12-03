pipeline{
    agent none
    stages {
        stage('Non-parallel stage'){
            agent{
                label "master"
            }
            steps{
                echo "This stage will execute first"
            }
        }
    
    stage('Run Tests'){
        parallel {
            stage('Test on Windows'){
                agent{
                    label "Windows_Node"
                }
                steps{
                    echo "Task1 on agent"
                }
            }
            stage('Test on Master'){
                agent{
                    label "master"
                }
                steps{
                    echo "Task1 on master"
                }
            }
        }
    }
}
}
