## Install Tibia with Desktop Menu Icon (Linux Ubuntu)

**INSTRUCTIONS**: 📋 Copy and paste below code in your terminal. 

````shell
cd ~ # Go to home directory
APP_DIR=~/tibia # Set variable APP_DIR to home/tibia
wget https://static.tibia.com/download/tibia.x64.tar.gz # download tibia from official website
tar -xvf tibia.x64.tar.gz # uncompress tar file into home folder
mv Tibia ~/tibia # rename it to tibia lowercase
rm tibia.x64.tar.gz # remove compressed file

# Add .desktop file to create an menu tibia app icon
cat << EOT | sudo tee /usr/share/applications/tibia.desktop > /dev/null 
[Desktop Entry]
Type=Application
Name=Tibia
Comment=Tibia Linux Client
Icon=${APP_DIR}/tibia.ico
Exec=${APP_DIR}/start-tibia-launcher.sh
Categories=Games;
Path=${APP_DIR}/
EOT

echo "Happy Play... =)"
````

## Download Minimap with Markers (Optional)
````shell
mkdir ~/tmp-minimap-with-markers
cd ~/tmp-minimap
wget https://tibiamaps.io/downloads/minimap-with-markers
unzip minimap-with-markers
mv minimap/* ~/.local/share/CipSoft\ GmbH/Tibia/packages/Tibia/minimap
rm -rd ~/tmp-minimap-with-markers
````
