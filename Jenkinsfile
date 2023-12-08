pipeline
{
    agent any
    stages
    {
        stage("Clean")
        {
            steps
            {
                echo " hello jenkin "
                sh ' rm -rf /var/lib/jenkins/workspace/jenkin1/* '
            }
        }
        stage("Clone")
        {
            steps
            {
                sh ' git clone -b master https://github.com/karthikjogi758/docker_jenkins.git '
            }
        }
        stage("Build")
        {
            steps
            {
                sh ' sudo docker build -t image1 /var/lib/jenkins/workspace/jenkin1/docker_jenkins '
            }
        }
        stage("Deploy")
        {
            steps
            {
                sh ' sudo docker run -it -d image1 '
            }
        }
    }
}
