check Swap:
sudo swapon --show {if NO output, No swap Space available}

Check active swap:
free -h

Check available Space in Hard Drive
df -h

Create a swap file in root directory
sudo fallocate -l 1G /swapfile

ls -lh /swapfile {check the size for swap}

Enable Swap file:
sudo chmod 600 /swapfile {Access only to root}
Verify: ls -lh /swapfile

mark the space as swap
sudo mkswap /swapfile

Enable the swap file:
sudo swapon /swapfile
Verify: sudo swapon --show
verify: free -h
