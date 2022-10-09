pipeline{
   agent{

         label 'Built-In Node'
         customWorkspace '/project'
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
             sh"cp -r index.html /var/www/html/"
             sh" chmod 777 /var/www/html/index.html" 
              }

          }   
  }


}
