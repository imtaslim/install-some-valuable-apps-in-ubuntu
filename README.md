# install-some-valuable-apps-in-ubuntu
Install Skype, VS-Code, postbird, tweak, chrome, brave, and many more

# Install Skype
~~~
sudo snap install skype
~~~

# Install VS-Code
~~~
sudo snap install code --classic
~~~

# Install postbird
~~~
sudo snap install postbird
~~~

# Install tweak
~~~
sudo snap install postbird
~~~

# Install universe repository
~~~
sudo add-apt-repository universe
~~~

# Install gnome-tool
~~~
sudo apt install gnome-tweak-tool
~~~

# Install gnome
~~~
gnome-tweaks
~~~

# Install extension for gnome (Optional)
~~~
sudo apt install $(apt search gnome-shell-extension | grep ^gnome | cut -d / -f1)
~~~

# Install chrome
~~~
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
~~~
then
~~~
sudo dpkg -i google-chrome-stable_current_amd64.deb
~~~

# Install Brave
First, install curl and allow apt over HTTPS:
~~~
sudo apt install apt-transport-https curl
~~~
Add the Brave repository key to your system:
~~~
curl -s https://brave-browser-apt-release.s3.brave.com/brave-core.asc | sudo apt-key --keyring /etc/apt/trusted.gpg.d/brave-browser-release.gpg add -
~~~
And then add the Brave repository in the sources.list.d directory:
~~~
echo "deb [arch=amd64] https://brave-browser-apt-release.s3.brave.com/ stable main" | sudo tee /etc/apt/sources.list.d/brave-browser-release.list
~~~
Now update the system and install Brave:
~~~
sudo apt update && sudo apt install brave-browser
~~~
