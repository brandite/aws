### Amazon Web Services

#### Amazon Free Tier
* [Amazon Free Tier](http://aws.amazon.com/free/)

#### Concepts
* What is "the cloud"?
* What is SSH
* What is a keypair?
* What's an AMI (Amazon machine instance) ?
* What is an "instance"
* What is EBS (Elastic Block Store)?
* What is sudo?
* What is a port (in tcp/ip)?
* What is RTFM?



#### Log of my steps

1. Created my account (pitosalas@mac.com)
1. Signed up for AWS - gave my credit card information
1. Watched the EC2 Video
1. Clicked "Launch Instance"
1. Select "Amazon Linux"
1. Select "Review and Launch"
1. Click "Launch"
1. Create a keypair called aws-demo
1. Click "Launch" again
1. Click on name of instance
1. Click to connect to the instance
1. Change mode of the pem file: chmod 400 aws-demo.pem
1. Run SSH with the indicated command

Yay! Success

#### Now, lets try running some software

1. Update software: 
	* sudo yum update
	* sudo yum remove ruby
	* sudo yum -y install make gcc ruby-devel
	* sudo yum install ruby
	* sudo gem install io-console
1. Verify:
	* Verify Ruby is present $ ruby -v
	* Verify gem is present $ gem -v
	* Verify python is present $ python -v
	* Verify java is present $ java -version
1. Make a dummy rails app
	* cd ~
	* sudo gem install rails --no-ri --no-rdoc
	* sudo yum install sqlite-devel
	* sudo yum install -y ruby20-devel gcc-c++
	* sudo gem install therubyracer
	* rails new hello
	* cd hello/
	* Uncomment gem therubyracer in Gemfile
	* Add to Gemfile: gem 'oj'
    * Add to Gemfile: gem 'oj_mimic_json'
    * bundle
	* rails s
1. Add a security group to allow inbound connections on port 3000


#### Random Tips
* On mac, to show hidden files in filel open, type cmd-shift-.


