Nexus installation
------------------
Step 1: Login to your Linux server and update the yum packages. Also install required utilities.
    sudo yum update -y
    sudo yum install wget -y
Step 2: Install OpenJDK 1.8
    sudo yum install java-1.8.0-openjdk.x86_64 -y
Step 3: Create a directory named app and cd into the directory.
    sudo mkdir /app && cd /app
Step 4: Download the latest nexus. You can get the latest download links fo for nexus from here.
    sudo wget -O nexus.tar.gz https://download.sonatype.com/nexus/3/latest-unix.tar.gz
    Untar the downloaded file and rename the folder
        sudo tar -xvf nexus.tar.gz
        sudo mv nexus-3* nexus
Step 5: As a good security practice, it is not advised to run nexus service with root privileges. So create a new user named nexus to run the nexus service.
    sudo adduser nexus
    Change the ownership of nexus files and nexus data directory to nexus user.
        sudo chown -R nexus:nexus /app/nexus
        sudo chown -R nexus:nexus /app/sonatype-work
Step 6: Open /app/nexus/bin/nexus.rc file
    sudo vi  /app/nexus/bin/nexus.rc
    Uncomment run_as_user parameter and set it as following.
        run_as_user="nexus"
step 7: if you want to change nexus configurations change here
    sudo vi /app/nexus/bin/nexus.vmoptions

Running Nexus as a System Service
    Create a nexus systemd unit file.
        sudo vi /etc/systemd/system/nexus.service
Manage Nexus Service
    Execute the following command to add nexus service to boot.
        sudo chkconfig nexus on
To start the Nexus service, use the following command.
    sudo systemctl start nexus

Sonatype Nexus not Starting [Troubleshooting]
    Execute the following command and see the actual error.
        journalctl -xe
