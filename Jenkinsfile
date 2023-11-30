pipeline
{
    agent any
    stages
    {
        stage("Clone")
        {   
            steps
            {
                sh ' sudo rm -rf /var/lib/jenkins/workspace/Docker/* '
                sh ' sudo git clone https://github.com/karthikjogi758/docker_jenkins.git '
            }
        }
        stage("Build")
        {
            steps
            {
                sh ' sudo docker build -t app /var/lib/jenkins/workspace/Docker/Docker-jenkins-tasks  '
            }
        }
        stage("Run")
        {
            steps
            {
                sh ' sudo docker run -it -d app '
            }
        }
    }
}
