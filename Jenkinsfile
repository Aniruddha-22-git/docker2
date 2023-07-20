pipeline{
  agent{
    label('built-in')
  }
  stages{
    stage('volume'){
      steps{
               sh "git clone https://github.com/Aniruddha-22-git/docker2.git -b 23q2 /mnt/23q2-vol"
        sh "docker run -itdp 91:80 -v /mnt/23q2-vol:/usr/local/apache2/htdocs --name 23q2-vol httpd"
        sh "docker exec 23q2-vol chmod -R 777 /usr/local/apache2/htdocs"  
      }
    }
  }
}
