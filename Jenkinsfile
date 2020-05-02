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
        stage('continousdeployment')
        {
            steps
            {
                sh label: '', script: ' scp -i /home/jenkins/qakey.ppk  /home/jenkins/workspace/declar/webapp/target/webapp.war root@100.24.3.40:/usr/local/tomcat/webapps/qq.war'
            }
        }
        
    }
 }   
