# ELB with stickiness Example
Terraform v0.12.25

The example launches a web server, installs nginx, creates an ELB for instance. It also creates security groups for the ELB and EC2 instance. 
To run, configure your AWS provider as described in https://www.terraform.io/docs/providers/aws/index.html

Run this example using:
1) deploy
    terraform apply -auto-approve
outputs:
 url_addr = example-elb-11.us-west-2.elb.amazonaws.com
    
2) verify
  Wait a couple of minutes for the EC2 userdata to install nginx, and then type the ELB DNS Name from outputs in your browser and see the nginx welcome page
  curl http://url_addr
outputs:
  nginx 

3) undeploy
   terraform destroy -auto-approve

