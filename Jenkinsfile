pipeline{
   agent{
      label {
         label '172.31.33.31'
         customWorkspace '/home/ec2-user/project/'
      }
   }
   stages{
       stage('install httpd'){
          steps{
           sh"sudo yum install httpd -y"
           sh"sudo service httpd start"
             }
          } 
       stage('copy the file'){
          steps{   
             sh"chmod -R 777 /home "
             sh"cp -r /home/ec2-user/project/* /var/www/html/"
             sh" chmod 777 /var/www/html/index.html" 
              }

          }   
  }


}
