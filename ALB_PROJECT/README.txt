1.Create 2 Security Group(ALL TCP & HTTP)
2.Create 2 EC2 instance with 2 different user data:

EX:-
#!/bin/bash
apt-get update -y
apt-get install -y apache2
systemctl start apache2
systemctl enable apache2

echo "<!DOCTYPE html>
<html>
<body style='background-color:green'>
<h1>Hi Pooja Saykar this is --> Server1</h1>
</body>
</html>" > /var/www/html/index.html          //update for second EC2 instance



3.Create Target group (attach both the created EC2 instance)
4.Create Application load balancer(attached created Target group)

Once application Load balancer is ACTIVE by using ALB DNS name we can check out load balancing.


