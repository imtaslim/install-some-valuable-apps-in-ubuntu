# Some-valuable-Command-for-ubuntu
Install Skype, VS-Code, postbird, tweak, chrome, brave, and many more

# Install Skype
~~~
sudo snap install skype
~~~

# If snap is showing error then restart it
~~~
sudo systemctl start snapd
~~~
then
~~~
sudo systemctl enable snapd
~~~
if it doesn't solve the error then uninstall snap
~~~
sudo apt autoremove --purge snapd
~~~
then install again
~~~
sudo apt install snapd
~~~

# Install VS-Code
~~~
sudo snap install code --classic
~~~

# Install postbird
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

# Install tweak
~~~
gnome-tweaks
~~~

# Install extension for gnome (Optional)
~~~
sudo apt install $(apt search gnome-shell-extension | grep ^gnome | cut -d / -f1)
~~~

# Install chrome
first check wget
~~~
wget --version
~~~
then
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

# Install protonvpn
1. Get the DEB setup package for the ProtonVPN repository

Download the ProtonVPN DEB package
https://protonvpn.com/download/protonvpn-stable-release_1.0.1-1_all.deb

2. Install the ProtonVPN repo

Double-click downloaded DEB package to install the repo using your default package manager. 

3. Update the apt-get package list

Open Terminal and enter the command:
~~~
sudo apt-get update
~~~

4. Install the ProtonVPN Linux app

Last step! Enter:
~~~
sudo apt-get install protonvpn
~~~

# Install video player decoder if you have issue to play videos
~~~
sudo apt-get install ubuntu-restricted-extras
~~~
or
~~~
sudo apt-get install libavcodec58 libav-tools ffmpeg
~~~
then
~~~
sudo apt remove gstreamer1.0-vaapi
~~~

# For clear Cache
first check disk usage
~~~
journalctl --disk-usage
~~~
then
~~~
sudo journalctl --rotate
~~~
then clear cache
~~~
sudo journalctl --vacuum-time=2days
~~~

# Convert from docx file to pdf file
~~~
lowriter --convert-to pdf CV.docx
~~~

# Corvert from pdf file to png photo
~~~
pdftoppm CV.pdf CV -png
~~~
