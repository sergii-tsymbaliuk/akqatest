#Steps to start test task:

# 1. get the project with preconfigured vagrant file from github
git clone https://github.com/sergii-tsymbaliuk/akqatest.git

# 2. go to the project folder
cd akqatest

# 3. run the box with provisioning to properly instal docker, pull the packedged applicatin and run it a
vagrant up --provision

# 4. open in a browser the link below on host machine:
 http://192.168.56.101/

