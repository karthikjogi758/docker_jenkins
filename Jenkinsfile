pipeline
{
    agent any
    stages
    {
        stage ("clean")
        {
            steps
            {
                echo "hello jenkin"
                 sh 'rm -rf /var/lib/jenkins/workspace/jenkin1/*'
            }
        }
        stage ("clone")
        {
            steps
            {
                sh 'git clone -b master https://github.com/karthikjogi758/docker_jenkins.git'
            }
        }
        stage ("build")
        {
            steps
            {
                sh 'sudo docker build -t image2 /var/lib/jenkins/workspace/jenkin1/docker_jenkins'
            }
        }
        stage ("run")
        {
            steps
            {
                sh 'sudo docker run -it -d image2'
            }
        }
    }
}
