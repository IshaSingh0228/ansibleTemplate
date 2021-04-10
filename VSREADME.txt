Connecting ubuntu instance with vscode

Kepp the .pem file inside .ssh folder in computer
Download Remote SSH Plugin on VSCode
Add to SSH Targets
Then Type
ssh -i ~/.ssh/awskeypair.pem  ubuntu@ec2-52-14-186-207.us-east-2.compute.amazonaws.com
Hit Enter twice 
Allow Cionnections

Once the instance is added to targets list right click and open in new window 
Press Okay

Once instance is online , goto File>Open Folder and click on the Home/Ubuntu Directory

END