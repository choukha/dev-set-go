# dev-set-go
# 1. Reset & Re-install the WSL
https://winaero.com/reset-unregister-wsl-linux-distro-windows-10/

# 2. Reinstall Ubuntu using Microsoft Store
https://codefellows.github.io/setup-guide/windows/

# 3. Open Powershell and set WSL2
wsl --set-default-version 2

# 4. Install Keycahin for .ssh sharing
https://devblogs.microsoft.com/commandline/sharing-ssh-keys-between-windows-and-wsl-2/

 sudo apt-get update
 sudo apt-get install keychain


# 5. Copy SSH keys
cp -r /mnt/c/Users/<username>/.ssh ~/.ssh
chmod 600 ~/.ssh/id_ed25519

# 6. Then add the following line to your ~/.bashrc file

vi ~/.bashrc
--> Insert Key
--> Paste this at the end of file
eval ``keychain --eval --agents ssh id_ed25519

:wq!

# 7. Install Docker
https://newbedev.com/shell-install-docker-on-wsl-without-docker-desktop-code-example


# 8 . Add this to .bashrc
sudo service docker start
