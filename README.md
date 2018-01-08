# Cleo's Coding Exercise

Welcome to Cleo's programming evaluation. Within this package is an ansible playbook that will build a Wordpress site within AWS. It's your job to add to it.

## Assignment 1

This ansible playbook (main.yml) will create a wordpress site. It is your job to add to the Ansible code to create the first post to the site. 

Utilize the [Metaweather API](https://www.metaweather.com/api/) to retrieve the weather for Chicago, Illinois. Then use this information to create a post on your Wordpress site with the Weather information retrieved via Ansible.

## Assignment 2

Utilizing Ansible add SSL to your Wordpress site. Use [Let's Encrypt](https://letsencrypt.org/) to generate an SSL certificate and utilize it to enable HTTPS access to your site.

## Pre-requisites

To accomplish this assignment you'll need to have Ansible installed locally and have an AWS account

## Config

To make this ansible playbook work you'll need to fill out the config file in `ansible/vars/secrets.yml` with the appropriate informatn

* `aws_access_key` - the access key from your aws account
* `aws_secret_key` - the secret access key fromo your aws account
* `ssh_private_key_file` - the pem file you use for your aws keypair
* `aws_key_pair_name` - the name of your aws keypair
* `aws_subnet_id` - you'll need to create a VPC to build your wordpress site within. Once your VPC is built copy the subnet ID here
* `wp_admin_email` - the email used for the WP admin account. This can be whatever you want it to be
* `wp_admin_pass` - the passw used for the WP admin account. This can be whatever value you want it to be
* `mysql_root_password` - the password for the root account of the MySQL DB used by Wordpress. This can be whatever value you want it to be
* `wp_db_password` - the password for the WP account of the MySQL DB used by Wordpress. This can be whatever value you want it to be
