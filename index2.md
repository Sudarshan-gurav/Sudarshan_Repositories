step to install mysql on local machine :

 steps: install mysql-server packeage install
   
   $ sudo apt-get update

   $ sudo apt-get install mysql-server
	
       after hiting above tab one window has popup it ask the password.

   $ systemctl status mysql.service
  
 If MySQL is not running, then start it with 
 
  $ sudo systemctl start mysql.

  $ mysql -u root -p password 



