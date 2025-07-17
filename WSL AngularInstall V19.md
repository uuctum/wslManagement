# upgrade linux 

sudo apt update
sudo apt upgrade

# Install NodeJS from NodeSource

1. Install the cURL utility, which we will use to download the PPA repository. Skip this step if you have it installed:

        sudo apt install curl

2. Run the following to download the Node.js package. Replace 22.x with your desired version number:

        sudo curl -fsSL https://deb.nodesource.com/setup_22.x | sudo -E bash -

3. Update your system repository to synchronize the package:

        sudo apt update

4. Install Node.js and NPM by running these commands subsequently:

        sudo apt-get install nodejs -y
        sudo apt-get install npm

   Upgrade npm 

        sudo npm install -g npm@11.1.0    

5. Verify that Node.js and NPM are successfully installed by querying their version numbers with these commands:

        sudo nodejs -v
        sudo npm -v


# Install Angular V19

        sudo npm install -g @angular/cli

# Set Global git information

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

git config --global user.email "ustun.uctum@axis-it.com"
git config --global user.name "Ustun Uctum"
