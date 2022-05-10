# To create SSH key We can either use RSA or id_25519 Encryption but rsa is safe

# Create SSH key using rsa

ssh-key-gen -t rsa -b 4096 -C "lohiyalavarthi95@gmail.com"

# Now the key generated we need to let ssh agent know about our key and store it to this

# SSh-agent is mostly like wallet where it stores ssh keys

# To run ssh-agent we need to do

eval "$(ssh-agent -S) - This is not working in gitbash

# To run in git bash

eval ssh-agent

# Need to add ssh-agent now using

ssh-add ~/.ssh/id_rsa ~- Simply mean C:/users/lohit

# Try to login to github acccount and settings -> SSH KEYS and try to create new ssh key and copy the ssh key id_rsa.pub that we generated in our system to github account

# to read id_rsa.pub in our file, we have to do cat ~/.ssh/id_rsa this will output contents in the file id_rsa.pub and we can copy that content and paste in github new sshkey field

# Try to test it now by doing

ssh -T git@github.com

# Basically the above command tells that we are going to use ssh key to access github.com

# if we want to clone from the github all we can do is just use git clone git@github.com:LohithaYalavarthi/Hooks-Concepts.git
