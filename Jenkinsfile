pipeline
{
    agent any
    stages
    {
        stage('continousdownload')
        {
            steps
            {
               git 'https://github.com/iosjsk/download.git' 
            }
        }
        stage('continous build')
        {
            steps
            {
                sh label: '', script: 'mvn package'
            }
        }
        }
        
 }
