# React App & deploy with Docker and Nginx on an AWS EC2 Ubuntu

in local:
  git clone https://github.com/imHarry404/hk-tic-tac-toe-react.git
  open vs code in project folder
    npm i
    npm run
**Access on [http://127.0.1:3000]/(http://localhost:3000/)**


##to run on ubuntu /aws ec2 instance
make sure node is installed on machine if not
**sudo apt install nodejs -y**

git clone https://github.com/imHarry404/hk-tic-tac-toe-react.git
cd hk-tic-tac-toe-react
npm i # to install all the packages
npm start  # it will start the react app on 

###access the app using public ip on 3000 port of the machine, make sure to enable 3000 inboud rule in sg.



### to contanerized it
install these softwares on ubuntu machine
file is present in repo
give execute permission

**chmod +x  prep-req.sh**

##wait till it finishes.
Now create a Dockerfile in project folder, already on repo

###Create an nginx/nginx.conf file in the root folder of your project with command : 
sudo vi nginx/nginx.conf

file is present in repo


Now:
Build and Run Docker Container
**docker build -t hk-react-app .
docker run -d -p 3000:80 hk-react-app
**





