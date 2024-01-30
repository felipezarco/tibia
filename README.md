# Install Tibia with Desktop Menu Icon (Linux Ubuntu)

````shell
APP_DIR=~/tibia
wget https://static.tibia.com/download/tibia.x64.tar.gz
tar -xvf tibia.x64.tar.gz
mv Tibia ~/tibia

echo "Adding menu desktop icon"
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
