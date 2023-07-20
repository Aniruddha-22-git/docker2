pipeline{
  agent{
    label('built-in')
  }
  stages{
    stage('volume'){
      steps{
        sh "git clone https://github.com/Aniruddha-22-git/docker2.git -b 23q1 /mnt/23q1-vol"
        sh "docker run -itdp 81:80 -v /mnt/23q1-vol:usr/local/apache/htdocs --name 23q1-vol httpd
        sh "docker exec 23q1-vol chomd -R 777 usr/local/apache2/htdocs"
      }
    }
  }
}
