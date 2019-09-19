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
install the mpapis public key. You’ll need it to avoid errors while downloading RVM.
