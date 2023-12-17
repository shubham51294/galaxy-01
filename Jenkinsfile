pipeline {
     agent{
        label {
            label "qa"
            customWorkspace "/mnt/gal-3"
            }
          }
     stages {
         stage ("one") {
              steps {
                  sh "sudo rm -rf *"
                  sh "sudo yum install git -y"
                  sh "sudo git clone https://github.com/shubham51294/galaxy-01.git -b 2023Q2"
				  }
				}
		 stage ("two") {
                       steps{ 
		                  sh "sudo yum install httpd -y"
				  sh "sudo systemctl start httpd"
				  sh "sudo cp -r galaxy-01/index.html /var/www/html/"
				  sh "sudo chmod -R 777 /var/www/html/index.html"
                           }
                      }
             }
}


