# myalerts-login
Send email alert on SSH or direct login attempt.

## Usage
Just install it, and you will receive emails to `root@localhost` if someone logins through SSH or tries to login from tty.
Note that your system must use `rsyslog` for this to work properly.
I recommend you to redirect root's email address to your own in `/etc/aliases` unless you won't receive these emails. (alternatively you can change it directly in `/etc/rsyslog.d/myalerts-login.conf`)

## Installation
- You can either [download](https://github.com/tamas646/myalerts-login/raw/main/myalerts-login_1.0.0_all.deb) and install the deb package or use the source code and setup it yourself.

- If you wish, you can install it from my apt repository too:

  ```sh
  sudo echo "deb http://apt.ptamas.hu/main/ ./" > /etc/apt/sources.list.d/apt.ptamas.list
  wget -O- https://apt.ptamas.hu/ptamas-pub.gpg |sudo apt-key add -
  apt update && apt install myalerts-login
  ```
