# InSync Nagios Theme
InSync Nagios Theme is a web theme that is designed to beautify the open source [Nagios Core] monitoring and alerting engine with another open source Bootstrap dashboard [AdminLTE]. 

We have done the hardwork for you to easily implement Nagios Core Dashboard with a user friendly navigation panel with AdminLTE.

# Pre-requisites
You need to first install Nagios Core.
Installation of Nagios Core is not covered in the document

SSH in to your Nagios Core server as root and access /usr/local/nagios/ folder.
```sh
[root@localhost /]$ cd /usr/local/nagios/
```
Makes sure you have a folder called 'share'.
This includes all files which are used in Nagios dashboard.
```sh
[root@localhost nagios]$ ls -l | grep share
drwxr-xr-x  18 root   root   4096 Jan 26 09:11 share
```

# Installation
1. Take a backup of the existing 'share' folder. So if you want you can revert back to the original site.
```sh
[root@localhost nagios]$ mv share/ share-original/
```
2. Access /tmp directory
```sh
[root@localhost nagios]$ cd /tmp
```

3. Download InSync Nagios theme.
```sh
[root@localhost tmp]$ git clone https://github.com/insyncit/insync-nagios-theme.git
```

4. Copy /tmp/insync-nagios-theme/share to /usr/local/nagios/share
```sh
[root@localhost tmp]$ cp -fr /insync-nagios-theme/share /usr/local/nagios/share
```

Your copy of the InSync Nagios Theme is now installed on your Nagios server.

Open up your favourite browser and access http://localhost/nagios

Enjoy!!!

[Nagios Core]: <https://www.nagios.org/projects/nagios-core/>
[AdminLTE]: <https://adminlte.io/>