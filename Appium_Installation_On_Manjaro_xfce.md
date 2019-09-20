# Install java
```sh
pacman -Ss openjdk
sudo  pacman -Ss extra/jdk8-openjdk
```

# Decalring JAVA_HOME variable in .bashrc
Check  JAVA_HOME variable exists or not
```sh
echo $JAVA_HOME
```
then... on .bashrc type
```sh
export JAVA_HOME="/usr/lib/jvm/java-8-openjdk"
export PATH="$PATH:$JAVA_HOME/bin"
```
Check whether java is accessible or not
```sh
java -version
```

# Install Apache Ant
https://www-us.apache.org/dist//ant/binaries/apache-ant-1.10.7-bin.tar.gz

Copy it on a location, in case i’ve copied it on /usr/local/bin/ant/ and then set the path variable of ANT_HOME
```sh
export ANT_HOME=usr/local/bin/ant
export PATH="$PATH:$ANT_HOME/bin
```
Check the install
```sh
ant  -version
```
Then if output shows then go to ant directory and type
```sh
ant -f fetch.xml -Ddest=system
```

# Insatall APACHE MAVEN
https://www-us.apache.org/dist/maven/maven-3/3.6.2/binaries/apache-maven-3.6.2-bin.tar.gz

Copy it on /usr/local/bin/ and set path according to this
```sh
export MAVEN_HOME="/usr/local/bin/apache-maven-3.6.2"
export PATH="$PATH:$MAVEN_HOME/bin"
```
Check installation
```sh
mvn  -v
```
# Install RVM
install the [mpapis public key](https://keybase.io/mpapis). You’ll need it to avoid errors while downloading RVM.
```sh
gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
```
Then, proceed to install RVM with Ruby:
```sh
\curl -sSL https://get.rvm.io | bash -s stable --ruby
source /home/rahul/.rvm/scripts/rvm
```
Once this is done, proceed to update RubyGems and Bundler:
```sh
gem update --system
gem install -no-rdoc-no-ri bundler
gem update
gem cleanup
```
# Installing Node.js
Install LinuxBrew first
```sh
pacman -Syu # CAUTION: this updates the whole system
pacman -S base-devel
sh -c "$(curl -fsSL https://raw.githubusercontent.com/Linuxbrew/install/master/install.sh)"
```
Add path
```sh
export  PATH=”/home/linuxbrew/.linuxbrew/bin”
```
On .profile and .bash_profile, because of [This](https://github.com/Linuxbrew/brew/issues/711) issue
```sh
echo 'export PATH="/home/linuxbrew/.linuxbrew/bin:$PATH"' >>~/.profile
echo 'export MANPATH="/home/linuxbrew/.linuxbrew/share/man:$MANPATH"' >>~/.profile
echo 'export INFOPATH="/home/linuxbrew/.linuxbrew/share/info:$INFOPATH"' >>~/.profile
```
Then Check if brew installed properly or not
```sh
brew doctor
```
After installing Linuxbrew...
```sh
brew install node
```
# Install GRUNT
```sh
npm install -g grunt grunt-cli
```
# Install Appium
```sh
npm install -g appium
npm install wd
npm install -g appium-doctor
```
Check if there is any problem on the installation of appium or not
```sh
Appium-doctor
```
To start appium
```sh
appium
```
