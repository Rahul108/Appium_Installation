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
